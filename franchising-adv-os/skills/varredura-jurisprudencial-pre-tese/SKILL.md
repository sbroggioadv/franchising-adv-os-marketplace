---
name: varredura-jurisprudencial-pre-tese
description: "GATE ⭐ BLOQUEANTE antes de redigir QUALQUER tese de franquia. Varre TJSP (foco), STJ e STF na fonte ANTES de escrever, via WebSearch/WebFetch nativos (Firecrawl/Perplexity só fallback), para confirmar se a tese escolhida (não-concorrência/bandeira, COF deficiente, royalties/fundo, multa rescisória, arbitragem, concorrência desleal) está alinhada ao entendimento ATUAL e detectar virada de jurisprudência. Classifica a tese em CONSOLIDADA / MAJORITÁRIA C/ DIVERGÊNCIA / EM DISPUTA / DESFAVORÁVEL e recomenda seguir, ajustar ou reconsiderar. Output: teses confirmadas + alertas. Liga ao validador-franquia. Use SEMPRE antes de redigir, ou ao dizer varredura jurisprudencial, essa tese de franquia ainda vale, como está o entendimento do TJSP, virou a jurisprudência, conferir antes de peticionar."
---

# VARREDURA-JURISPRUDENCIAL-PRE-TESE ⭐

> Camada 1 e **GATE BLOQUEANTE**: nenhuma tese de franquia é redigida antes desta varredura confirmar que ela está viva no tribunal que vai julgar. Mitiga o pior risco: **improcedência por tese desatualizada**.

## Anexos obrigatorios (context/)
- `context/jurisprudencia-franquia.md` — corpus de teses-âncora ✅ + gaps a verificar ao vivo. **Ponto de partida, não dispensa a checagem.** `grep -niE "TEMA|TESES-ANCORA|pesquisar ao vivo" context/jurisprudencia-franquia.md`.
- `context/lei-13966-2019.md` e `context/cpc-faixas-franquia.md` — para amarrar a tese ao dispositivo.

## Objetivo
Dada a tese escolhida + o tribunal competente, confirmar com **busca real** que ela está validada por julgado recente (12-24 meses) e sinalizar divergência/virada — **antes** de qualquer linha de peça.

## Quando ativar
- **Sempre** antes de redigir petição/contestação/recurso (auto-chain do `franchising-master`).
- Quando o operador pedir conferência de entendimento atual sobre uma tese de franquia.

## Diferença para `validador-franquia` e `anti-alucinacao-juris-franquia`
Esta valida se a tese **ainda vence** (varredura ANTES de redigir). As outras validam se a citação **existe/confere** na peça pronta. Complementares e todas bloqueantes.

## Metodologia

1. **Input:** tese central (ex.: não-concorrência pós-contratual com limite; COF entregue < 10 dias anula; royalties = prazo decenal CC 205) + **tribunal competente** (foco **TJSP** — 1ª/2ª Câmaras Reservadas de Direito Empresarial) + lado + período-alvo (privilegiar 2025-2026).

2. **Listar as âncoras do corpus** que sustentam a tese (artigo da 13.966 + julgado ✅ do anexo) — elas guiam a busca.

3. **Buscar julgados recentes (busca real).** Ordem de ferramentas: **WebSearch/WebFetch nativos primeiro**; Firecrawl/Perplexity **só fallback** se disponíveis. Queries-modelo (adaptar):
   - `"TJSP Câmara Reservada Direito Empresarial franquia não concorrência 2025"`
   - `"TJSP COF circular oferta franquia 10 dias anulação 2025"` (esaj/jusbrasil)
   - `"STJ franquia royalties prazo prescricional"` + `site:stj.jus.br` quando útil
   - `"STJ franquia cláusula penal redução equitativa art 413"`
   - Pendência: `"STF Tema 1389 ARE 1.532.603 franquia competência julgamento"`

   **Coletar por julgado:** órgão, nº (CNJ ou REsp), data, sentido (favorável/contrário ao lado), trecho da ementa. **Só registrar o que a busca realmente retornar.**

4. **Classificar a tese:**
   | Status | Critério |
   |---|---|
   | **✅ CONSOLIDADA** | Lei + julgados recentes do TJSP/STJ no mesmo sentido, sem divergência relevante |
   | **🟢 MAJORITÁRIA C/ DIVERGÊNCIA** | Maioria favorável, mas há corrente contrária (câmara isolada / outra Turma) — blindar a peça |
   | **🟡 EM DISPUTA** | Tema afetado/pendente ou racha real — resultado incerto; avisar o cliente |
   | **🔴 DESFAVORÁVEL** | TJSP/STJ recentes contra a tese → improcedência provável; reconsiderar ângulo |

5. **Recomendar:** **seguir** (consolidada) / **ajustar** (blindar contra divergência, trocar fundamento) / **reconsiderar** (propor ângulo alternativo do corpus).

## Pontos quentes a SEMPRE checar (jun/2026)
> Sinalizar quando a tese tocar nestes (do anexo de jurisprudência):
- **Não-concorrência SEM limitação territorial** — a tese de nulidade existe (falta de raio/território invalida), mas **falta acórdão TJSP verificado** com o parâmetro espacial nominado. Buscar ao vivo antes de afirmar o limite de raio/território.
- **STF Tema 1389 (ARE 1.532.603/PR)** — competência da Justiça Comum em franquia: **confirmar se houve julgamento de mérito** ou se segue em repercussão geral/suspensão. Não citar como definitivo sem checar.
- **Decadência de 4 anos (CC 178)** na anulação por vício da COF — fundamento legal firme, mas **julgado de apoio específico de franquia precisa ser aberto**.
- **Multa rescisória + CC 413** — redução é **ordem pública mas NÃO automática** (STJ REsp 1.898.738 é o foundational, não é caso de franquia). Em peça, a aplicação franquia-específica vem das Câmaras Empresariais do TJSP — confirmar o julgado.
- **Cobrança de valores = decenal (CC 205)** vs **anulação = decadência 4 anos (CC 178)** — não trocar os prazos.

## Output — Relatório de varredura
```
RELATÓRIO DE VARREDURA JURISPRUDENCIAL — GATE PRÉ-TESE
Tese analisada: <...>   Tribunal competente: <ex: TJSP – 1ª CRDE>
Período varrido: <...>  Ferramentas: <WebSearch/WebFetch/Firecrawl/Perplexity>

JULGADOS ENCONTRADOS (só o que a busca confirmou):
| Órgão | Nº | Data | Sentido | Trecho |
|---|---|---|---|---|

CLASSIFICAÇÃO: <✅ CONSOLIDADA / 🟢 MAJORITÁRIA C/ DIVERGÊNCIA / 🟡 EM DISPUTA / 🔴 DESFAVORÁVEL>
DIVERGÊNCIA DETECTADA: <...>     TEMA PENDENTE RELEVANTE: <ex: STF Tema 1389>
RECOMENDAÇÃO: <SEGUIR / AJUSTAR / RECONSIDERAR>  → <como blindar / ângulo alternativo>
DECISÃO DO GATE: <LIBERADO para redigir / RETIDO até ajuste>
```

## Regra anti-halucinação
1. **Nunca inventar** julgado, número de processo ou ementa. Só reportar o que o WebFetch/WebSearch retornou.
2. Julgado de TJSP → confirmar nº CNJ + data abrindo o inteiro teor (esaj). Achados 🟡 do anexo (fonte secundária) **não viram munição** sem abertura do inteiro teor.
3. Busca sem julgado recente do TJSP → registrar "sem julgado recente localizado; apoiar em STJ + sinalizar risco" — não preencher com julgado presumido.
4. Esta skill **não dispensa** `anti-alucinacao-juris-franquia` / `validador-franquia` na peça pronta.

## Integração
Acionada por `franchising-master` (auto, antes de toda peça) e por `triagem-franchising`. Upstream: `competencia-foro-arbitragem-franquia` (fornece o tribunal). Downstream: libera (ou retém) a skill de peça. Fecha o ciclo com `validador-franquia` antes da `suprema-corte-franchising`. Cross-link soft: `juris-adv-os` (sugestão, nunca execução).
