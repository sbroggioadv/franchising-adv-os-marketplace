---
name: concorrencia-desleal-bandeira
description: "Redige a acao do FRANQUEADOR contra o ex-franqueado que continua usando a marca/identidade/sistema apos a rescisao ('virou a bandeira'). Pedido PRINCIPAL de abstencao (cessacao do uso de marca, trade dress, insignia e know-how) + perdas e danos + lucros cessantes, com base na LPI (Lei 9.279/96) art. 195 III/IV/V/XI/XII (concorrencia desleal), art. 209 caput + §1º (reparacao + liminar antes da citacao) e art. 210 (lucros cessantes pelo criterio mais favoravel), na clausula de bandeira do contrato e na COF art. 2º XV. A liminar de abstencao vai pela tutela-urgencia-abstencao. Use quando o operador disser o ex-franqueado continua com a minha marca, virou a bandeira, esta usando meu sistema depois da rescisao, concorrencia desleal, uso indevido de marca, /acao-franquia bandeira."
---

# CONCORRENCIA-DESLEAL-BANDEIRA

> Camada 5 (Contencioso/conhecimento). Acao do FRANQUEADOR (titular da marca/rede) contra o ex-franqueado que opera com a marca/sistema apos o fim do contrato. Pedido principal de abstencao. Gestao processual (competencia/arbitragem) obrigatoria ANTES.

## Anexos obrigatorios (context/)
- `context/lpi-concorrencia-desleal.md` — **art. 195** (III desvio de clientela, IV expressao/sinal, V nome/titulo/insignia, XI/XII know-how confidencial mesmo apos o contrato), **art. 209** (caput reparacao + **§1º liminar** antes da citacao + §2º apreensao), **art. 210** (lucros cessantes). **grep + ler a faixa.**
- `context/lei-13966-2019.md` — **art. 2º XV** (pos-contrato: know-how/segredos + atividade concorrente). `grep -n "XV"`.
- `context/jurisprudencia-franquia.md` — **TEMA C** e **TEMA G** (abstencao de marca/desfazimento da bandeira; limite do exercicio da atividade). So ✅.

## Objetivo
Fazer cessar o uso indevido da marca/sistema pelo ex-franqueado e reparar o dano, sem extrapolar para a vedacao da propria atividade (que a jurisprudencia nao admite).

## Quando ativar
- Rescindido (ou em vias de) o contrato, o ex-franqueado **continua usando** marca, identidade visual, layout, insignia, sistema e know-how da rede.
- Ha desvio de clientela por meio fraudulento ou uso de segredo de negocio pos-contrato.

## Metodologia
1. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia` — arbitragem (art. 7º §1º; havendo clausula, urgencia pre-arbitral ao Judiciario, Lei 9.307 art. 22-A; depois aos arbitros, 22-B) → foro com pertinencia (CPC 63, Lei 14.879/2024; sem CDC entre as partes). Carregar `base-legal-13966`.
2. **`varredura-jurisprudencial-pre-tese` ANTES da tese** — confirmar o entendimento atual (abstencao de marca x nao-concorrencia ampla).
3. **Enquadrar a concorrencia desleal (LPI art. 195):** identificar os incisos aplicaveis — **V** (uso indevido de nome comercial/titulo/insignia — nucleo do "virar a bandeira"), **IV** (sinal/expressao de propaganda criando confusao), **III** (meio fraudulento para desviar clientela), **XI/XII** (uso de conhecimentos/segredos confidenciais a que teve acesso por contrato, **mesmo apos o termino**) — casa com a COF art. 2º XV-a.
4. **Pedido PRINCIPAL de abstencao** (obrigacao de nao fazer): cessar o uso de marca, trade dress, insignia, layout, sistema e know-how; descaracterizar o ponto comercial e devolver manuais (TJSP Ap. 1032315-87.2020.8.26.0576 · 1ª CRDE · Rel. Des. Cesar Ciampolini ✅; abstencao de marca acolhida em TJSP ODONTOCOMPANY 1005968-68.2017.8.26.0011 · 2ª CRDE · Rel. Des. Ricardo Negrao ✅).
5. **LIMITE estrutural (nao errar):** pede-se abstencao de **marca/trade dress/sistema**, **nao** a interrupcao da atividade — o ex-franqueado pode continuar no mesmo ramo de forma independente (TEMA C/B ✅). Pedido amplo demais e cortado.
6. **Liminar:** **LPI art. 209 §1º** permite ao juiz, **antes da citacao**, "determinar liminarmente a sustacao da violacao", mediante caucao se necessario; cumular com **CPC 300** (probabilidade + perigo) e **astreintes (CPC 537)** → redigir a urgencia pela `tutela-urgencia-abstencao`. §2º: apreensao em reproducao flagrante de marca registrada.
7. **Perdas e danos + lucros cessantes:** **LPI art. 209 caput** (perdas e danos) + **art. 210** (lucros cessantes pelo **criterio mais favoravel ao prejudicado**: I beneficios que teria auferido; II beneficios do violador; III remuneracao/royalty que pagaria pela licenca). Quantum geralmente iliquido → conhecimento/liquidacao.
8. **Cross-link de marca:** registro/titularidade e validade da marca → `marca-inpi-adv-os`.

## Entrega obrigatoria final
- Inicial redigida (fatos do uso indevido + enquadramento LPI 195 por inciso + pedido principal de abstencao com limites + perdas e danos + lucros cessantes art. 210 + requerimento de liminar 209 §1º/CPC 300 + astreintes) + checklist (registro da marca, contrato/clausula de bandeira, prova do uso atual) + foro/vara ou clausula arbitral.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). Pedido de abstencao **com limites** — nunca vedar a atividade em si. CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente. A liminar redige-se pela `tutela-urgencia-abstencao`; titularidade da marca via `marca-inpi-adv-os`. Fecha pela `suprema-corte-franchising` (R1-R4).
