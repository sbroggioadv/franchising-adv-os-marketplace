---
name: acao-rescisao-franquia
description: "Redige a acao do FRANQUEADOR que forca a rescisao do contrato de franquia por inadimplemento, pelo rito comum (CPC 318/319), CUMULANDO (CPC 327): cobranca dos valores em aberto quando iliquidos (royalties percentuais sobre faturamento, perdas e danos vao pelo conhecimento, nao pela execucao), multa contratual (clausula penal redutivel por equidade — CC 413, STJ REsp 1.898.738), perdas e danos comprovados e ABSTENCAO de uso de marca/sistema (nao-concorrencia/bandeira, com limites validos). Valor da causa = soma dos pedidos (CPC 292 II+V+VI). Use quando o operador disser quero rescindir a franquia, acao de rescisao, o franqueado nao paga royalties, vou processar o franqueado, rescisao por inadimplemento, /acao-franquia rescisao."
---

# ACAO-RESCISAO-FRANQUIA

> Camada 5 (Contencioso/conhecimento). Acao condenatoria do FRANQUEADOR que resolve o contrato por inadimplemento do franqueado e cumula cobranca, multa, perdas e danos e abstencao. Gestao processual (competencia/arbitragem) obrigatoria ANTES.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§2** (rescisao/rito comum): CPC 318 (procedimento comum), 319 (inicial), 327 (cumulacao), 292 I/II/V/VI + §3º (valor da causa); **§1.2** (iliquidez: CPC 783, 786 §ú, 803 I — o que NAO executar). **grep + ler a faixa.**
- `context/lei-13966-2019.md` — art. 2º XV-b / XXI (nao-concorrencia / limitacao a concorrencia), art. 7º §1º (arbitragem). `grep -n "XV" / "XXI" / "Art\. 7"`.
- `context/jurisprudencia-franquia.md` — **TEMA D** (multa + CC 413, STJ REsp 1.898.738 ✅) e **TEMA B** (limites da nao-concorrencia, TJSP ODONTOCOMPANY ✅). So ✅.

## Objetivo
Produzir inicial solida que decrete a rescisao por inadimplemento e recupere tudo o que e devido, sem cair em improcedencia por pedido vago, por cobrar valor iliquido na execucao ou por nao-concorrencia ampla demais.

## Quando ativar
- Franqueado inadimplente (royalties, fundo, taxas) ou em descumprimento grave; o franqueador quer pôr fim ao contrato e ser ressarcido.
- Ha uso indevido de marca/sistema a cessar (encadear com `tutela-urgencia-abstencao` e `concorrencia-desleal-bandeira`).

## Metodologia
1. **Gestao processual SEMPRE (C1) ANTES de redigir:** acionar `competencia-foro-arbitragem-franquia` — **arbitragem PRIMEIRO** (ha clausula compromissoria? art. 7º §1º Lei 13.966 + Lei 9.307/96; se valida, o Judiciario e incompetente, CPC 337 X, salvo tutela pre-arbitral CPC 305) → depois **foro de eleicao** (CPC 63 com pertinencia, Lei 14.879/2024; sem ressalva consumerista — `natureza-empresarial-nao-cdc`). Carregar `base-legal-13966`.
2. **Enquadrar o inadimplemento:** resolucao por inadimplemento (CC 475 — base material; confirmar redacao via `validador-franquia`, nao consta verbatim no anexo) + clausula resolutoria do contrato. Demonstrar mora e descumprimento.
3. **Rito comum (CPC 318) + inicial (CPC 319):** juizo, qualificacao das partes (distinguir **PF x PJ** — o franqueado comprou como PF e abriu empresa?), fato e fundamentos, pedido especificado, valor da causa, provas.
4. **Cumulacao (CPC 327):** "e licita a cumulacao, em um unico processo, contra o mesmo reu, de varios pedidos" — requisitos do §1º (compativeis, mesmo juizo, procedimento adequado); §2º procedimentos diversos → empregar o **procedimento comum**. Desenho tipico:
   - (a) **Rescisao** do contrato por inadimplemento;
   - (b) **Cobranca** dos valores em aberto — **iliquidos vao AQUI** (royalties percentuais sobre faturamento que dependem de apurar/pericia; perdas e danos), pois titulo executivo nao comporta liquidacao (CPC 803 I) — o que for liquido pode ir por execucao (`execucao-contrato-franquia`);
   - (c) **Multa** contratual (clausula penal);
   - (d) **Perdas e danos** (so o que for **comprovado** — nao se presume);
   - (e) **Abstencao** de uso de marca/identidade/sistema/know-how → liminar via `tutela-urgencia-abstencao`; fundamento de concorrencia desleal via `concorrencia-desleal-bandeira`.
5. **`varredura-jurisprudencial-pre-tese` ANTES de cravar as teses** (multa, nao-concorrencia, base de calculo) — entendimento atual TJSP/STJ.
6. **Multa (clausula penal):** exigivel, mas **redutivel por equidade** — CC 413 e dever do juiz / direito do devedor, **ordem publica** (STJ REsp 1.898.738 ✅); **nao ha reducao automatica**. Dimensionar com razoabilidade para nao ser cortada.
7. **Abstencao/nao-concorrencia com LIMITES:** o pedido de nao usar marca/bandeira/metodologia prospera; **mas nao pode aniquilar o exercicio da atividade** do ex-franqueado (TJSP ODONTOCOMPANY 1005968-68.2017.8.26.0011 · 2ª CRDE · Rel. Des. Ricardo Negrao ✅; padrao aceito ~2 anos + territorio). Pedir abstencao de **marca/trade dress/sistema**, nao a interrupcao total da atividade.
8. **Valor da causa (CPC 292):** rescisao = valor do ato/parte controvertida (**II**); cobranca corrigida (**I**); indenizatoria = valor pretendido (**V**); cumulacao = **soma** de todos (**VI**); §3º o juiz corrige de oficio.

## Entrega obrigatoria final
- Inicial redigida ponta a ponta (fatos + inadimplemento + pedidos cumulados a/b/c/d/e + multa dimensionada + valor da causa somado + provas) + checklist de documentos (contrato, COF, demonstrativo do debito, prova do uso indevido) + indicacao de foro/vara **ou** da clausula arbitral aplicavel.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). Multa **nao** e automatica nem irreduzivel (CC 413). Nao-concorrencia **com limites**. Valor iliquido **nao** vai por execucao. CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente. Calculo de debitos/atualizacao → cross-link `calculosjudiciais-adv-os`/`execucao-adv-os`. Fecha pela `suprema-corte-franchising` (R1-R4).
