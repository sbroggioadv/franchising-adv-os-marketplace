---
name: reconvencao-franquia
description: "Redige a reconvencao SIDE-AWARE em litigio de franquia (CPC 343), conexa com a acao principal ou com o fundamento da defesa, na mesma peca da contestacao. Tipico do FRANQUEADO-reu: reconvir para devolucao de taxas/royalties por COF viciada (Lei 13.966 art. 2º §2º + art. 4º) ou indenizacao por falha de suporte/exclusividade territorial. Tipico da FRANQUEADORA-re: reconvir para cobrar debitos do contrato + multa contratual. Resposta do reconvindo em 15 dias (343 §1º); a reconvencao independe da contestacao (§6º) e prossegue ainda que extinta a acao principal (§2º). Use quando o operador disser quero reconvir, reconvencao na franquia, alem de me defender quero cobrar/pedir devolucao, vou pedir de volta os royalties na mesma acao."
---

# RECONVENCAO-FRANQUIA

> Camada 5 (Contencioso/conhecimento). Pretensao propria do reu na mesma peca, **side-aware** (franqueado OU franqueadora). Acoplada a `contestacao-franquia`. Gestao processual obrigatoria.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **CPC 343** (caput conexao; §1º resposta 15d; §2º independe da acao principal; §6º independe de contestacao); 292 (valor da causa da reconvencao); 327 (cumulacao). **grep + ler a faixa.**
- `context/lei-13966-2019.md` — art. 2º §2º + art. 4º (devolucao corrigida — reconvencao do franqueado); art. 2º IX (royalties/fundo — reconvencao da franqueadora). `grep -n`.
- `context/jurisprudencia-franquia.md` — TEMA E (devolucao por COF viciada), TEMA D (multa/CC 413). So ✅.

## Objetivo
Deduzir, na mesma relacao processual, a pretensao propria do reu conexa ao contrato/COF — devolucao (franqueado) ou debitos+multa (franqueadora) — sem perder a economia processual.

## Quando ativar
- O reu, alem de se defender, tem **credito ou pedido proprio** ligado ao mesmo contrato/COF.
- Conexao com a acao principal (mesmo contrato) ou com o fundamento da defesa.

## Metodologia
1. **Definir o LADO** e checar a **conexao** (CPC 343 caput): pretensao "conexa com a acao principal ou com o fundamento da defesa".
2. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia` (mesmo juizo da principal; se ha clausula arbitral valida, atencao — a reconvencao no Judiciario tambem pode esbarrar na arbitragem) + `base-legal-13966`.
3. **`varredura-jurisprudencial-pre-tese` ANTES da tese** (devolucao / multa).
4. **Montar a pretensao por LADO:**
   - **FRANQUEADO-reu reconvem para:** (a) **devolucao** de taxa de filiacao + royalties + demais valores **corrigidos** por **COF viciada** (omissa/falsa/fora do prazo de 10 dias) — Lei 13.966 **art. 2º §2º + art. 4º** (verbatim no anexo); (b) **indenizacao** por descumprimento de suporte/treinamento/exclusividade territorial (perdas e danos comprovados). Cuidar do contraponto de convalidacao (STJ REsp 1.881.149 ✅).
   - **FRANQUEADORA-re reconvem para:** (a) **cobrar debitos** do contrato (royalties/fundo/taxas) — iliquidos vao por conhecimento, nao por execucao; (b) **multa** contratual (clausula penal, redutivel por equidade — CC 413, STJ REsp 1.898.738 ✅); (c) perdas e danos comprovados.
5. **Procedimento (CPC 343):** proposta na contestacao; o **autor-reconvindo e intimado, na pessoa do advogado, para responder em 15 dias** (§1º); **§2º** a desistencia/extincao da acao **nao obsta** o prosseguimento da reconvencao; **§6º** o reu pode reconvir **independentemente** de contestar.
6. **Valor da causa da reconvencao (CPC 292):** proprio, conforme o pedido (cobranca = soma corrigida I; devolucao/indenizacao = valor pretendido V; cumulacao = soma VI).

## Entrega obrigatoria final
- Reconvencao redigida (fatos da pretensao propria + fundamento por lado + pedido certo + valor da causa proprio + provas, esp. **pericia contabil** para apurar valores) na mesma peca da contestacao + confirmacao da conexao e do prazo de resposta do reconvindo.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). Conferir **conexao** e **arbitragem** antes de reconvir no Judiciario. Devolucao exige prejuizo/tempo razoavel; multa nao e automatica (CC 413). CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente. Calculo dos valores → cross-link `calculosjudiciais-adv-os`. Fecha pela `suprema-corte-franchising` (R1-R4).
