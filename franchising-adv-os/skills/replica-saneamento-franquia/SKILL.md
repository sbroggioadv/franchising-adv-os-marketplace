---
name: replica-saneamento-franquia
description: "Redige a REPLICA do autor a contestacao no litigio de franquia (impugna a defesa de merito, refuta as preliminares do art. 337 — esp. arbitragem e foro — e responde aos fatos impeditivos/modificativos/extintivos alegados pelo reu) e contribui para o SANEAMENTO do processo (CPC 357): fixacao dos pontos controvertidos, distribuicao do onus da prova e requerimento de provas, com destaque para a PERICIA CONTABIL que apura royalties/fundo sobre o faturamento. Use quando o operador disser vou replicar, replica a contestacao, fui intimado da contestacao, organizar as provas, saneamento, requerer pericia contabil dos royalties, especificacao de provas na franquia."
---

# REPLICA-SANEAMENTO-FRANQUIA

> Camada 5 (Contencioso/conhecimento). Resposta do autor a contestacao + organizacao do processo para a instrucao. Acoplada a `contestacao-franquia`/`reconvencao-franquia`. Gestao processual obrigatoria.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§5/§6**: CPC 337 (preliminares a refutar — X arbitragem, foro), 341 (impugnacao especificada), 343 §1º (resposta a reconvencao em 15d). **grep + ler a faixa.** *(A replica em si — CPC 350/351 — e o saneamento — CPC 357 — NAO constam verbatim no anexo: confirmar redacao via `validador-franquia` antes de selar.)*
- `context/lei-13966-2019.md` — art. 2º IX (royalties/fundo — objeto da pericia) e §2º/art.4º (vicio da COF, se a defesa o invocou). `grep -n`.
- `context/jurisprudencia-franquia.md` — TEMA E (fundo de propaganda / prestacao de contas), TEMA A (sem CDC). So ✅.

## Objetivo
Neutralizar a defesa e deixar o processo maduro para a instrucao: refutar preliminares, responder o merito indireto e fixar com clareza o que sera provado — sobretudo a apuracao contabil dos valores.

## Quando ativar
- O autor foi intimado da contestacao (defesa indireta — fatos impeditivos/modificativos/extintivos — ou preliminares).
- O reu reconveio (responder a reconvencao em 15 dias — CPC 343 §1º).
- O juiz abre vista para especificacao de provas / vai sanear o processo.

## Metodologia
1. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia` — **se o reu nao alegou a convencao de arbitragem na contestacao, houve renuncia** (CPC 337 §6º); se alegou, refutar a existencia/validade/alcance da clausula (atencao ao Kompetenz-Kompetenz, Lei 9.307 art. 8º). Carregar `base-legal-13966`/`natureza-empresarial-nao-cdc`.
2. **Refutar as preliminares (CPC 337):** rebater incompetencia/foro abusivo (pertinencia — Lei 14.879/2024), arbitragem, incorrecao do valor, inepcia etc., uma a uma.
3. **Replicar o merito:** responder aos **fatos impeditivos, modificativos ou extintivos** e a eventual defesa indireta; manter a coerencia com a impugnacao especificada (CPC 341) — o autor reafirma os fatos da inicial e ataca a versao do reu. *(A replica decorre dos arts. 350/351 do CPC — confirmar a redacao verbatim via `validador-franquia`, pois nao consta no anexo.)*
4. **Responder a reconvencao (se houver):** prazo de **15 dias** na pessoa do advogado (CPC 343 §1º) — contestar a pretensao propria do reu (devolucao por COF viciada ou debitos+multa).
5. **`varredura-jurisprudencial-pre-tese` ANTES de fechar as teses** controvertidas.
6. **Contribuir ao SANEAMENTO (CPC 357 — moldura; confirmar redacao via `validador-franquia`):** sugerir ao juizo (a) **fixacao dos pontos controvertidos** (ex.: houve inadimplemento? a COF foi viciada? a multa e excessiva? os royalties incidem sobre qual base?); (b) **distribuicao do onus da prova** pela regra do **CPC 373** (sem inversao consumerista — franqueado nao e consumidor); (c) **provas** a produzir.
7. **PERICIA CONTABIL (o nucleo probatorio):** requerer pericia para **apurar royalties/fundo sobre o faturamento** (valores percentuais sao iliquidos e dependem de apuracao) e conferir a base de calculo. Tese de apoio (TEMA E): o **fundo de propaganda** tende a ser indevido se a franqueadora nao comprova o uso publicitario / a prestacao de contas — *os precedentes especificos de fundo estao marcados **🟡** no anexo; abrir o inteiro teor ao vivo (`varredura-jurisprudencial-pre-tese`) antes de citar numero*. Indicar **assistente tecnico** e **quesitos** — cross-link `calculosjudiciais-adv-os`.

## Entrega obrigatoria final
- Replica redigida (refutacao de preliminares + resposta ao merito indireto + resposta a reconvencao se houver) + minuta de contribuicao ao saneamento (pontos controvertidos + onus da prova CPC 373 + provas requeridas, com **pericia contabil** e quesitos sobre royalties/fundo).

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). **CPC 350/351/357 nao constam do anexo — confirmar redacao ao vivo antes de citar verbatim.** Onus da prova pelo CPC 373 (sem inversao do CDC — art. 1º). Nunca a 8.955/94 como vigente. Apuracao de valores → cross-link `calculosjudiciais-adv-os`. Fecha pela `suprema-corte-franchising` (R1-R4).
