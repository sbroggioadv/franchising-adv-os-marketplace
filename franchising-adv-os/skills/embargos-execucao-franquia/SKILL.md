---
name: embargos-execucao-franquia
description: "Defesa SIDE-AWARE do executado na execucao do contrato de franquia: embargos a execucao (CPC 914 e ss. — prazo/garantia a confirmar verbatim no anexo, 🟡), excesso de execucao, NULIDADE do titulo por iliquidez (CPC 803 I — royalties %-faturamento que dependem de apurar faturamento nao podiam ser executados), exceptio non adimpleti contractus (CPC 787 — franqueador que cobra royalties sem provar que cumpriu suporte/sistema), e parcelamento do executado (CPC 916, 🟡 confirmar). Use quando o operador disser embargar a execucao, defender o franqueado executado, excesso de execucao, o titulo e iliquido, a franqueadora nao cumpriu, parcelar a divida da execucao, contestar a penhora."
---

# EMBARGOS-EXECUCAO-FRANQUIA

> Camada 6 (execucao) — lado da defesa. **Side-aware**: defende o **executado** (em regra o franqueado; pode ser a franqueadora). Espelho de `execucao-contrato-franquia`. Primeiro definir o lado, depois montar a defesa.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§1 (803 I nulidade por iliquidez ✅; 787 contraprestacao ✅; 786 §u liquidez)**, **§3 (827/829 fluxo)**, **PENDENCIAS (914-920 embargos e 916 parcelamento — 🟡 a confirmar verbatim)**. `grep -niE "803|787|embargos|914|916|919" context/cpc-faixas-franquia.md`.
- `context/lei-13966-2019.md` — **art. 2o IX-a/c, XVIII** (a verba executada e licita/exigivel?), **art. 1o** (relacao empresarial — sem CDC, sem inversao do onus na defesa).
- `context/financeiro-dre.md` — **§1.2/§6** o que torna royalties/fundo iliquidos (base de calculo) — municao do excesso/nulidade.
- `context/jurisprudencia-franquia.md` — **Tema E** (COF viciada → defesa/reconvencao) e **Tema D** (multa reduzivel CC 413) — so apos confirmar.

## Objetivo
Opor a defesa adequada do executado: extinguir/anular a execucao quando o titulo nao e liquido (803 I), reduzir o excesso, opor a *exceptio* (787) e, em ultimo caso, viabilizar o parcelamento (916) — sempre com o lado definido.

## Quando ativar
- O cliente foi **citado em execucao** do contrato de franquia (royalties, fundo, multa, debitos) e quer se defender.
- Gatilhos: "embargar", "defender o franqueado executado", "excesso de execucao", "titulo iliquido", "a franqueadora nao deu suporte", "parcelar a execucao".

## Metodologia

### 1. Gestao + lado (Camada 1)
Definir **o lado** (executado = franqueado ou franqueadora). `competencia-foro-arbitragem-franquia`: **ha clausula de arbitragem?** O merito do credito pode ser arbitral — verificar se cabe alegar a convencao (a execucao em si corre no Judiciario).

### 2. Via e prazo — embargos a execucao (CPC 914 e ss. — 🟡 CONFIRMAR)
> ⚠️ As regras de **embargos a execucao (CPC 914 a 920)** estao marcadas como **🟡 nao conferidas verbatim** no anexo (PENDENCIAS). Antes de fixar prazo, garantia e efeito, **confirmar a faixa verbatim** (a referencia e: prazo de **15 dias** da juntada do mandado, **independem de garantia do juizo**, **sem efeito suspensivo automatico** — atribuivel pelo juiz; CPC 919). **Nao afirmar numero de artigo/prazo sem abrir o anexo/fonte.**

### 3. Materia de defesa (eventualidade — alegar tudo)
**(a) Nulidade do titulo por iliquidez — CPC 803, I ✅ (a defesa mais forte em franquia):**
> **Art. 803, I** — "e **nula a execucao** se o titulo executivo extrajudicial **nao corresponder a obrigacao certa, liquida e exigivel**".

Royalties **percentuais sobre faturamento** que dependem de **apurar o faturamento** sao **iliquidos** -> nao podiam ser executados; a execucao e nula nessa extensao (cross-check `execucao-contrato-franquia` §3 + financeiro-dre §1.2). O credor deveria ter ido a cobranca (785).

**(b) Excesso de execucao:** o valor cobrado supera o devido — atacar o **demonstrativo (798 §u)**: indice, juros, capitalizacao, termos. Apontar o **valor que entende correto** (requisito do excesso). Multa contratual eventualmente **reduzivel por equidade — CC 413** (Tema D 🟡, ordem publica, **nao** automatica — so apos confirmar).

**(c) Exceptio non adimpleti contractus — CPC 787 ✅:**
> **Art. 787** — quem so deve mediante **contraprestacao do credor** pode opor que o credor **nao adimpliu**; o exequente devia **provar que adimpliu** sob pena de extincao.

Franqueado opoe que a **franqueadora nao prestou suporte/supervisao/sistema** prometidos (COF art. 2o XIII) — descumprimento que afasta a exigibilidade dos royalties. Liga a `acao-anulatoria-cof`/reconvencao quando ha vicio da COF.

**(d) Premissa anti-CDC:** franqueado **nao e consumidor** (art. 1o) — **sem inversao do onus**, sem hipossuficiencia presumida; o onus da defesa segue a regra empresarial.

### 4. Parcelamento do executado — CPC 916 (🟡 CONFIRMAR)
> ⚠️ **CPC 916** (deposito de **30% do valor** + parcelamento em **ate 6 prestacoes mensais** com juros/correcao) esta **🟡 a confirmar verbatim** no anexo. Opcao do executado que **reconhece** o debito e quer parcelar — **confirmar requisitos e prazo na fonte antes de redigir**. Incompativel com embargos (renuncia ao restante).

## Entrega obrigatoria final
- Embargos a execucao (ou peca de defesa adequada) com o lado definido, alegando na ordem: nulidade por iliquidez (803 I), excesso de execucao (com valor correto), *exceptio* (787) e, se for a estrategia, o parcelamento (916) — com os prazos/garantia **confirmados na fonte** (914-920/916 sao 🟡).

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. **914-920 e 916 sao 🟡 — confirmar verbatim antes de citar prazo/garantia** (regra anti-alucinacao do anexo). CC 413 (Tema D) so apos `varredura-jurisprudencial-pre-tese`. Lado definido antes de redigir. Gestao por `competencia-foro-arbitragem-franquia`. Entrega fecha pela `suprema-corte-franchising`.
