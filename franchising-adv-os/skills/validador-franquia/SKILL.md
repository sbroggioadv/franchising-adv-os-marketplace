---
name: validador-franquia
description: "GATE anti-alucinação de SAÍDA. Cruza cada dispositivo, súmula, tese e acórdão da peça de franquia contra o context/ (lei-13966, cpc-faixas, jurisprudencia ✅, lpi) ANTES de selar. Extrai todas as citações, verifica uma a uma e marca ✅ VALIDADA / 🟡 NÃO CONFIRMADA / 🔴 INEXISTENTE-ERRADA, bloqueando o envio se houver qualquer 🔴 ou 🟡 não resolvido. Checklist anti-alucinação: Lei 8.955/94 NUNCA como vigente (revogada art. 9º); distinção CDC (franqueador×franqueado fora art. 1º MAS rede responde ao consumidor final REsp 1.426.578/SP); jurisprudência só ✅ com número + órgão. Use SEMPRE antes de protocolar/entregar, e quando o usuário disser valida as citações, esse acórdão de franquia existe, confere os dispositivos, audita a peça, antes de selar, esse artigo da Lei de Franquia está certo."
---

# VALIDADOR-FRANQUIA — Gate anti-alucinação de saída

> Camada 1. **Último filtro** antes de qualquer peça de franquia ser selada. Bloqueante: o que não confirma no `context/`, **não passa**. Acoplado ao guard global `anti-alucinacao-juridica`.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — confere artigo/inciso/§ da Lei de Franquia (verbatim).
- `context/cpc-faixas-franquia.md` — confere dispositivos processuais (CPC, Lei 9.307/96, Lei 14.879/2024) marcados ✅.
- `context/jurisprudencia-franquia.md` — confere julgado: só ✅ (verificado) entra; 🟡 (fonte secundária) exige WebFetch ao vivo.
- `context/lpi-concorrencia-desleal.md` — confere LPI art. 195/209/210 (bandeira/concorrência desleal).

## Objetivo
Garantir que **nenhum dispositivo, súmula, tese ou acórdão** entre na peça sem bater com o `context/` (ou, para juris, sem verificação ao vivo). Cruzar cada citação, marcar veredito e bloquear o que falhar.

## Quando ativar
- **Sempre** antes de selar/protocolar qualquer peça de franquia (auto-chain, antes da `suprema-corte-franchising`).
- Quando o operador pedir conferência de citações/dispositivos.

## Diferença para `varredura-jurisprudencial-pre-tese`
Aquela confirma se a tese **ainda vence** (antes de redigir). Esta confirma se a citação **existe e confere** (na peça pronta). Ambas bloqueantes.

## Metodologia

1. **Extrair todas as citações** da peça: cada dispositivo (Lei 13.966, CPC, CC, Lei 9.307/96, LPI), cada súmula, cada Tema, cada acórdão (nº CNJ/REsp + órgão + relator). Montar tabela — uma linha por item.

2. **Verificar uma a uma:**
   | Tipo de citação | Onde conferir |
   |---|---|
   | Artigo da Lei 13.966/2019 | `lei-13966-2019.md` (grep o art.) — texto bate? |
   | CPC / Lei 9.307 / Lei 14.879 | `cpc-faixas-franquia.md` (só itens ✅; 🟡 = confirmar verbatim) |
   | CC (205/178/413/475) | dispositivo legal vigente — confirmar redação/nº (475 e parte do CC são 🟡 no anexo → checar) |
   | LPI 195/209/210 | `lpi-concorrencia-desleal.md` |
   | Súmula / Tema / acórdão | `jurisprudencia-franquia.md` (só ✅) **+ WebFetch ao vivo** para qualquer 🟡 |

3. **CHECKLIST ANTI-ALUCINAÇÃO (armadilhas obrigatórias):**
   - 🔴 **Lei 8.955/94 citada como vigente** → ERRO. Está **revogada** (Lei 13.966/2019 art. 9º). Remapear para o dispositivo equivalente da 13.966.
   - 🔴 **CDC afirmado "de forma absoluta" como inaplicável** → erro de distinção. Correto: franqueador × franqueado **fora** do CDC (Lei 13.966 art. 1º + STJ REsp 1.602.076/SP, 632.958/AL ✅), **MAS** a rede **responde solidariamente perante o consumidor final** (CDC 14/18 — STJ **REsp 1.426.578/SP** ✅). Verificar qual eixo a peça invoca.
   - 🔴 **Não-concorrência sem limite de prazo/território afirmada como válida** → a jurisprudência exige **limites** e não pode aniquilar o exercício da atividade (TJSP ODONTOCOMPANY 1005968-68.2017 ✅). Parâmetro espacial nominado sem julgado aberto = 🟡.
   - 🔴 **Multa rescisória afirmada como reduzível automaticamente** → CC 413 é ordem pública mas **não automática** (STJ REsp 1.898.738 ✅, foundational — não é caso de franquia).
   - 🔴 **Prazos trocados:** cobrança de royalties/fundo/multa = **decenal CC 205**; anulação por vício da COF = **decadência 4 anos CC 178**.
   - 🔴 **Arbitragem alegada de ofício / fora da contestação** → CPC 337 §5º (juiz não conhece de ofício) e §6º (silêncio = renúncia). Em peça de defesa, a preliminar 337 X deve estar no 1º momento.
   - 🟡 **Súmula 5/7 STJ** em REsp → conferir (interpretação de cláusula e reexame de prova **não** ensejam REsp — barreira central em franquia).

4. **Marcar veredito por item:**
   - **✅ VALIDADA** — `context/` (ou fonte oficial ao vivo) confirma número + teor + vigência.
   - **🟡 NÃO CONFIRMADA** — não conferiu conclusivo, ou item 🟡 do anexo (fonte secundária / dispositivo não capturado verbatim). Ação: substituir por âncora ✅ equivalente, remover, ou reescrever "(confirmar na íntegra antes de citar)".
   - **🔴 INEXISTENTE/ERRADA** — não existe, teor não bate, ou é armadilha conhecida. Ação: **remover** imediatamente.

5. **Veredito final (bloqueante):**
   - **0 vermelho e 0 amarelo não resolvido → LIBERADO** para a `suprema-corte-franchising`.
   - **Qualquer 🔴 ou 🟡 pendente → BLOQUEADO.** Devolver a peça com a lista do que corrigir. Não liberar sob nenhuma hipótese.

## Output — Relatório de validação
```markdown
## Relatório de validação — franquia
**Peça:** [tipo] · **Lado:** [franqueador/franqueado] · **Data:** [YYYY-MM-DD]

| # | Citação na peça | Tipo | Conferido em | Veredito | Ação |
|---|---|---|---|---|---|
| 1 | Lei 13.966 art. 2º §2º | dispositivo | lei-13966-2019.md | ✅ VALIDADA | manter |
| 2 | "Lei 8.955/94 vigente" | dispositivo | — | 🔴 ERRADA | remover (revogada, art. 9º) |
| 3 | STJ REsp 1.426.578/SP | acórdão | jurisprudencia-franquia.md ✅ | ✅ VALIDADA | manter |

### Resumo — ✅: N · 🟡: N · 🔴: N
### VEREDITO: [✅ LIBERADO p/ Suprema Corte | 🔴 BLOQUEADO]
[Se bloqueado: lista numerada do que corrigir.]
```

## Proibições
1. **NUNCA liberar** peça com 🔴 ou 🟡 pendente.
2. **NUNCA** marcar ✅ acórdão sem fonte (anexo ✅ ou WebFetch oficial conferido).
3. **NUNCA** deixar passar a 8.955/94 como vigente nem o CDC "absoluto".
4. **NUNCA inventar** número de REsp/Tema/súmula para completar.

## Integração
Upstream: `franchising-master` chama em toda peça final, depois da redação e da `varredura-jurisprudencial-pre-tese`. Para juris pesada, aciona `anti-alucinacao-juris-franquia` (WebFetch). Downstream: só após ✅ a peça segue para `suprema-corte-franchising`.
