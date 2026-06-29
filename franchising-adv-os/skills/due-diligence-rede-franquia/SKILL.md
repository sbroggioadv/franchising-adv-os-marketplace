---
name: due-diligence-rede-franquia
description: "DIFERENCIAL (lado FRANQUEADO/comprador): avalia a SAUDE DA REDE antes da compra, a partir da COF e de fontes publicas — acoes judiciais relativas a franquia (art. 2o IV: a rede esta sendo processada? por que?), franqueados que se DESLIGARAM nos ultimos 24 meses (art. 2o X: rotatividade alta = sinal vermelho — contatar ex-franqueados), balancos dos 2 ultimos exercicios (art. 2o III: a franqueadora e financeiramente saudavel?), reputacao e maturidade. Emite RELATORIO DE RISCO da rede (verde/amarelo/vermelho), complementar a `auditoria-cof` (que olha o documento; esta olha a rede por tras dele). Use quando o operador disser investigar a rede de franquia, due diligence da franquia, a franqueadora e confiavel, quantos franqueados sairam, a rede tem processos, vale comprar essa franquia, checar a saude da franqueadora."
---

# DUE-DILIGENCE-REDE-FRANQUIA

> Consultivo (diferencial — defensivo). **Lado: franqueado/comprador** avaliando a rede **antes de comprar**. Complementa `auditoria-cof`: aquela audita o **documento**; esta investiga a **rede por tras dele** (litigios, churn, balancos, reputacao).

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2o IV (acoes judiciais), X (franqueados + desligados em 24 meses), III (balancos 2 exercicios)** — os incisos que alimentam a investigacao. `grep -niE "IV |X — |III —|24 meses|balanco" context/lei-13966-2019.md`.
- `context/jurisprudencia-franquia.md` — **Tema E** (omissao de litigio/disclosure -> anulacao) e **Tema A** (a rede responde ao consumidor final — risco reputacional) — so apos confirmar.
- `context/financeiro-dre.md` — leitura dos balancos da franqueadora (III) e sanidade do modelo (a unidade-modelo fecha?).

## Objetivo
Produzir um **relatorio de risco da rede** (verde/amarelo/vermelho) que diga ao comprador se a franqueadora e solida, litigiosa ou em deterioracao — antes de investir. A COF e a base; a verificacao ao vivo confirma.

## Quando ativar
- O cliente vai comprar uma franquia e quer saber se a **rede** e confiavel (alem do documento).
- Gatilhos: "due diligence da franquia", "investigar a rede", "a franqueadora e confiavel?", "quantos franqueados sairam", "a rede tem processos", "vale comprar essa franquia".

## Metodologia

### 1. Litigios da rede — art. 2o IV (+ verificacao ao vivo)
> **Art. 2o IV** — a COF deve indicar as **acoes judiciais relativas a franquia** que questionem o sistema ou possam comprometer a operacao (franqueador, controladoras, subfranqueador, titulares de marca/PI).

- Conferir o que a COF declara (IV) **e** verificar ao vivo (consulta processual publica nos TJs/STJ pelo CNPJ da franqueadora e ligadas). **Volume de acoes de ex-franqueados contra a franqueadora** = sinal vermelho (rede que litiga muito com a propria base).
- **Omissao de litigio relevante** na COF = vicio de disclosure -> alavancagem futura (Tema E 🟡) e ja um alerta de confiabilidade.

### 2. Churn — franqueados desligados em 24 meses (art. 2o X)
> **Art. 2o X** — relacao completa dos franqueados **e dos que se desligaram nos ultimos 24 meses**, com nomes, enderecos e telefones.

- **Rotatividade alta** (muitos desligamentos sobre o total) = bandeira vermelha. Calcular a proporcao desligados/ativos.
- **Acao recomendada:** contatar ex-franqueados da lista (X) — sao a fonte mais honesta sobre suporte real, faturamento real e relacao com a franqueadora.

### 3. Saude financeira — balancos (art. 2o III)
> **Art. 2o III** — balancos e demonstracoes financeiras da franqueadora dos **2 ultimos exercicios**.

- Ler os balancos (com apoio do `financeiro-dre`): a franqueadora tem **solidez** para entregar o suporte prometido? Patrimonio, endividamento, continuidade. Franqueadora fragil -> risco de suporte que nao vem (e de a rede ruir).

### 4. Maturidade e reputacao
- Tempo de rede, numero de unidades, ritmo de expansao (crescimento rapido demais sem estrutura = risco).
- Reputacao publica: reclamacoes de consumidores (lembrando que a rede **responde ao consumidor final** — Tema A), avaliacoes, presenca de marca (cross-link `marca-inpi-adv-os` para a situacao registral da marca — art. 2o XIV).

### 5. Semaforo de risco
Consolidar em **verde** (rede solida, baixo churn, sem litigio relevante), **amarelo** (pontos de atencao a esclarecer) ou **vermelho** (alto churn / muitos litigios de ex-franqueados / balanco fragil / omissoes na COF).

## Entrega obrigatoria final
- Relatorio de risco da rede: litigios (declarados x verificados ao vivo), indice de churn (desligados/ativos em 24m) com recomendacao de contatar ex-franqueados, leitura dos balancos (III), maturidade/reputacao, e **semaforo verde/amarelo/vermelho** com recomendacao. Achados de processo/numero **so apos verificacao real**.

## Guard
Nenhum dado de litigio/numero entra sem **verificacao ao vivo** (consulta processual real) — nunca afirmar "a rede tem X processos" sem fonte. Jurisprudencia (Temas A/E) so apos `varredura-jurisprudencial-pre-tese` + `validador-franquia`. Cross-link, nao duplicar: auditoria do documento -> `auditoria-cof`; marca -> `marca-inpi-adv-os`. Entrega fecha pela `suprema-corte-franchising`.
