---
name: anti-alucinacao-juris-franquia
description: "Guard local anti-alucinacao do plugin franchising, acoplado ao guard global anti-alucinacao-juridica. Bloqueia QUALQUER citacao de sumula/tese/tema/acordao/dispositivo que tente entrar em peca sem verificacao real; manda usar varredura-jurisprudencial-pre-tese (antes de redigir) + validador-franquia (antes de selar). Use antes de citar qualquer fundamento de franquia, ou quando o operador disser valida essa jurisprudencia, essa sumula esta vigente, esse acordao existe, esse tema existe, confere essa ementa, antes de citar, esse dispositivo ainda vale."
---

# ANTI-ALUCINACAO-JURIS-FRANQUIA — Guard local

> Camada 0. Trava de seguranca. Nenhuma citacao — legal ou jurisprudencial — entra em peca sem passar por aqui. Acoplada ao guard global `anti-alucinacao-juridica` (camada autossuficiente, independente do cwd).

## Anexos obrigatorios (context/)
- `context/jurisprudencia-franquia.md` — corpus com selos ✅/🟡; so ✅ e citavel; 🟡 = pista, exige abrir inteiro teor ao vivo — **grep do tema + ler a faixa**.
- `context/lei-13966-2019.md` — conferir existencia/redacao de dispositivo da lei vigente.
- `context/lpi-concorrencia-desleal.md` e `context/cpc-faixas-franquia.md` — conferir LPI 195/209 e dispositivos do CPC.

## Objetivo
Impedir que qualquer dispositivo, sumula, tese, tema ou acordao **inexistente, revogado, alterado ou nao verificado** entre numa peca de franquia. Veredito binario por citacao: **VALIDADO** ou **BLOQUEADO**.

## Quando ativar
Antes de inserir qualquer citacao numa peca/recurso/parecer; ou "valida essa jurisprudencia", "essa sumula esta vigente", "esse acordao/tema existe", "confere essa ementa", "antes de citar", "esse dispositivo ainda vale".

## Regras invioláveis (R-FRANQUIA)
1. **So ✅.** Nenhuma sumula/tese/tema/acordao/REsp/RE entra sem verificacao real na fonte (a URL/fonte oficial precisa abrir e o trecho/tese constar la). Achado **🟡** so vira municao depois de aberto o inteiro teor ao vivo.
2. **NUNCA a Lei 8.955/94 como vigente** — esta revogada (art. 9º da Lei 13.966/2019). Acordao antigo que aplica a 8.955 -> mapear para o artigo correspondente da 13.966.
3. **Distincao CDC obrigatoria.** Entre franqueador e franqueado **NAO ha relacao de consumo** (art. 1º; STJ REsp 1.602.076/SP). MAS a rede responde ao **consumidor final** (CDC 14/18; STJ REsp 1.426.578/SP). Tratar a nao-incidencia como "absoluta" e ERRO — bloquear.
4. **STF Tema 1389 (ARE 1.532.603/PR)** so como definitivo apos confirmar merito ao vivo (segue em repercussao geral/suspensao ate verificacao).
5. **Fundamentos legais** (CC 413/178/205, CPC 300/305/337 X/537/784 III, LPI 195/209, Lei 9.307/96 art. 4º §2º, Lei 13.966/2019) sao citaveis como lei vigente — conferir o numero/redacao no anexo antes de colar.

## Metodologia
1. Recebida uma citacao, classificar: dispositivo de lei ou jurisprudencia.
2. **Dispositivo:** grep no anexo (`lei-13966-2019.md` / `lpi-concorrencia-desleal.md` / `cpc-faixas-franquia.md`) — existe e esta vigente? Senao -> BLOQUEADO.
3. **Jurisprudencia:** achar em `jurisprudencia-franquia.md`. **✅** -> VALIDADO; **🟡** -> manda rodar `varredura-jurisprudencial-pre-tese` + abrir inteiro teor ao vivo; **nao consta** -> busca ao vivo obrigatoria (`WebSearch`/`WebFetch`; Firecrawl/Perplexity fallback) na fonte oficial (TJSP/STJ/STF).
4. **Acionar o guard global** `anti-alucinacao-juridica` em paralelo.
5. **Veredito por citacao:** VALIDADO (com fonte) ou BLOQUEADO (motivo: inexistente / revogado / 🟡 nao aberto / nao verificavel / 8.955 / CDC mal aplicado). Na duvida -> BLOQUEADO.

## Entrega obrigatoria final
- Lista de citacoes com veredito (VALIDADO/BLOQUEADO) + fonte/ponteiro + motivo do bloqueio. As bloqueadas saem da peca. Entrega o resultado para a `suprema-corte-franchising` (R3).

## Guard
Default no incerto e **BLOQUEAR**. Nada inventado, nada revogado, nada 🟡 sem conferencia ao vivo, nunca a 8.955/94, nunca CDC entre as partes. Trabalha junto com `varredura-jurisprudencial-pre-tese` (antes de redigir) e `validador-franquia` (antes de selar).
