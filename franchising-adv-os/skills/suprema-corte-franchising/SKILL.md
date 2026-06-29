---
name: suprema-corte-franchising
description: "Gate de qualidade final do plugin franchising. Aplica 4 validacoes (R1 fatos/partes/LADO/competencia-arbitragem, R2 fundamentacao na Lei 13.966/2019 vigente — nunca a 8.955/94 — e CDC nos dois eixos, R3 jurisprudencia real TJSP/STJ/STF apenas as ✅ verificadas, R4 forma/pedidos/multa/liminar/valor da causa) antes de qualquer entrega. Use SEMPRE antes de entregar COF, contrato, manual, notificacao, peca, recurso ou parecer; acionada pelo franchising-master ao fechar qualquer ato. Tambem quando o operador disser revisao final, valida antes de entregar, /revisao-final-franquia."
---

# SUPREMA-CORTE-FRANCHISING — Gate R1-R4

> Camada 0. Auditoria final obrigatoria de excelencia (default-on). Nenhuma entrega sai sem passar por aqui. Veredito: APROVADO / REVISAR / REPROVADO.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — conferir base na lei vigente (COF 23 incisos, prazo 10 dias, sancao §2º/art.4º, arbitragem art.7º §1º) — **grep do artigo + ler faixa**.
- `context/cpc-faixas-franquia.md` — rito/tutela/execucao/recursos/valor da causa.
- `context/lpi-concorrencia-desleal.md` — art. 195/209 (bandeira/abstencao).
- `context/jurisprudencia-franquia.md` — corpus com selos ✅/🟡; so ✅ entra.
- `context/metodologia-franchising.md` — gate R1-R4 (§4) e travas (§2).

## Quando ativar
SEMPRE como ultimo passo, antes de entregar qualquer artefato (COF, contrato, manual, peca, recurso, parecer). Acionada pelo `franchising-master` ao fechar o ato; ou "revisao final", "valida antes de entregar".

## As 4 validacoes
**R1 — Fatos / partes / LADO / competencia.** Os fatos batem com `memoria-de-caso-franquia`? Partes corretas (distingue **PF x PJ** — o franqueado comprou como PF e depois abriu a empresa?)? **Lado certo** (franqueador x franqueado)? **Ha clausula de arbitragem** (art. 7º §1º)? Se ha e e valida (art. 4º §2º Lei 9.307/96 — destaque em adesao), o Judiciario e incompetente (CPC 337 X), salvo tutela pre-arbitral (CPC 305). Foro de eleicao valido (sem CDC) — pertinencia exigida (Lei 14.879/2024).

**R2 — Fundamentacao na lei vigente.** Tudo na **Lei 13.966/2019** (NUNCA a 8.955/94 — revogada, art. 9º; acordao antigo mapeado para a lei nova)? **CDC nos dois eixos** (sem CDC entre franqueador e franqueado, art. 1º; rede responde ao consumidor final, CDC 14/18)? Dispositivos certos: CC 413 (multa redutivel por equidade — ordem publica), CC 178 (decadencia 4 anos / anulabilidade), CC 205 (cobranca decenal), CPC 300/305/537/784 III, LPI 195/209.

**R3 — Jurisprudencia real.** Todo acordao/sumula/tema passou pelo `validador-franquia` + `anti-alucinacao-juris-franquia` e consta de `jurisprudencia-franquia.md` como **✅**? Nenhuma citacao **🟡** sem abrir inteiro teor ao vivo; nada inventado. **STF Tema 1389 (ARE 1.532.603/PR)** so como definitivo apos confirmar merito ao vivo.

**R4 — Forma / pedidos.** Enderecamento, partes e pedidos completos e coerentes? **Multa** bem dimensionada e fundamentada (CC 413)? **Liminar** com base + periculum (CPC 300 + LPI 209 §1º) e **astreintes** (CPC 537)? **Nao-concorrencia/bandeira** com LIMITES validos (prazo + territorio; nao aniquila a atividade — ODONTOCOMPANY)? **COF** com os 23 incisos e prazo de 10 dias (art. 2º §1º)? **Valor da causa** correto?

## Metodologia
1. Rodar R1 -> R2 -> R3 -> R4 em ordem.
2. Marcar cada item OK / CORRIGIR.
3. Se CORRIGIR, devolver a skill de origem; nao entregar.
4. So liberar quando R1-R4 = OK.

## Entrega obrigatoria final
- Veredito (APROVADO / REVISAR / REPROVADO) + lista do que foi checado por round + correcoes exigidas.

## Guard
Na duvida em R3, default e remover/checar ao vivo. Lado errado, arbitragem ignorada ou competencia/foro errados = reprova em R1. Citar a 8.955/94 como vigente ou tratar franquia como consumo entre as partes = reprova em R2. Nao "passar pano".
