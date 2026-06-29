---
name: contrato-de-franquia
description: "Redige o contrato de franquia empresarial completo sob a Lei 13.966/2019 — objeto e licenca de marca, territorio/exclusividade, royalties e fundo de marketing, taxa de franquia, prazo e renovacao (art. 2o XXII), penalidades/clausula penal, nao-concorrencia e bandeira (remete a clausula-nao-concorrencia-e-bandeira), sublocacao (art. 3o) e foro/arbitragem (art. 7o §1o, remete a gestao). Natureza empresarial paritaria, sem CDC (art. 1o); assinado por 2 testemunhas = titulo executivo (CPC 784 III). Use quando o operador disser redigir/montar o contrato de franquia, minuta do contrato de franquia, clausulas do contrato de franquia, ou contrato-padrao da COF (XVI)."
---

# CONTRATO-DE-FRANQUIA

> Camada 2 — Formatacao da franquia. Contrato empresarial que transforma o que a COF declara em **obrigacao executavel**. Natureza paritaria, **sem CDC** (art. 1o). E o **contrato-padrao** que a COF anexa (art. 2o XVI).

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 1o** (objeto/licenca de PI + sem consumo/sem vinculo), **art. 2o** (IX royalties/fundo, VIII-b taxa, XV/XXI nao-concorrencia, XVI contrato-padrao, XVIII multas, XXII prazo/renovacao), **art. 3o** (sublocacao), **art. 7o §1o** (arbitragem) — **grep + ler a faixa**.
- `context/financeiro-dre.md` — §6.2: a **base de calculo** de royalties (IX-a) e fundo (IX-c) e transcrita do DRE para as clausulas financeiras (mesma base/percentual/periodicidade).
- `context/cpc-faixas-franquia.md` — **CPC 784, III** (titulo executivo: documento + 2 testemunhas; §4o e-assinatura com integridade dispensa testemunhas).
- `context/jurisprudencia-franquia.md` — Temas D (multa/CC 413), F (foro/arbitragem), H (prescricao) — so ✅.

## Objetivo
Produzir o contrato empresarial **ponta-a-ponta**, com clausulas que sustentem a operacao da rede E sobrevivam ao crivo judicial: licenca de marca, deveres reciprocos, taxas com base coerente ao DRE/COF, restritivas validas, foro/arbitragem definido — gerando, com 2 testemunhas, **titulo executivo** para a inadimplencia futura.

## Quando ativar
- O franqueador (ou o advogado de qualquer lado) precisa da minuta do contrato de franquia.
- Ja existe a COF/DRE e falta o contrato-padrao (art. 2o XVI) coerente com eles.

## Metodologia

### 1. Gestao processual ANTES de fechar foro/arbitragem
`competencia-foro-arbitragem-franquia` define a clausula de solucao de conflitos: **foro de eleicao** (CPC 63 + Lei 14.879/2024 exige pertinencia) **OU cláusula compromissoria de arbitragem** (art. 7o §1o + Lei 9.307/96). Sendo franquia contrato de adesao, a clausula arbitral deve observar o **art. 4o §2o da Lei 9.307/96** (destaque/visto especial do aderente), sob pena de nulidade (STJ REsp 1.602.076/SP ✅).

### 2. Estrutura de clausulas (montar bloco a bloco)
1. **Qualificacao das partes** — franqueador e franqueado, com CNPJ (se PJ ja constituida; se PF que abrira empresa, ver `aditivo-inclusao-pj`).
2. **Objeto e licenca de marca** — verbatim art. 1o: autoriza *"usar marcas e outros objetos de propriedade intelectual... ao direito de uso de metodos e sistemas... sem caracterizar relacao de consumo ou vinculo empregaticio"*. O franqueador deve ser **titular ou requerente** ou autorizado (art. 1o §1o — cross-link `marca-inpi-adv-os`).
3. **Territorio e exclusividade** — area de atuacao, exclusiva/preferencial, vendas fora do territorio (coerente com COF XI).
4. **Taxa de franquia** — valor **fixo, unico**, na assinatura (COF VIII-b); concessao de uso + treinamento + suporte de implantacao.
5. **Royalties** — **% sobre o faturamento bruto** (modelo padrao) com base/periodicidade **identicas a COF IX-a e ao DRE**.
6. **Fundo de marketing/propaganda** — base de calculo (COF IX-c); **verba afetada** a marketing da rede, **nao receita livre** da franqueadora; direito do franqueado a **prestacao de contas** (`prestacao-contas-fundo-marketing`).
7. **Obrigacoes da franqueadora** — suporte, supervisao, treinamento, manuais, inovacao (COF XIII a-f).
8. **Obrigacoes do franqueado** — seguir manuais/padrao, comprar de fornecedores homologados (COF XII), cotas minimas (XIX), padrao arquitetonico (`manual-arquitetonico`).
9. **Prazo e renovacao** — **especificacao precisa** do prazo e condicoes de renovacao (COF/art. 2o XXII).
10. **Penalidades / clausula penal** — situacoes e valores (COF XVIII). A multa e **redutivel por equidade** (CC 413 — STJ REsp 1.898.738 ✅: reducao e *"dever do juiz e direito do devedor"*, ordem publica, nao automatica) — calibrar para nao ser manifestamente excessiva.
11. **Nao-concorrencia e bandeira** — **remeter a `clausula-nao-concorrencia-e-bandeira`** (engine das restritivas com limites validos de prazo + territorio + clausula de bandeira pos-rescisao).
12. **Sublocacao** (se houver) — art. 3o: legitimidade de qualquer parte para renovar a locacao; o aluguel ao franqueador **pode ser superior** ao que paga ao proprietario desde que **previsto na COF e contrato** e **sem onerosidade excessiva** (art. 3o par. unico).
13. **Confidencialidade / know-how** — protecao de segredos durante e **apos** o contrato (COF XV-a; LPI art. 195 XI).
14. **Transferencia/sucessao** (COF XVII), **rescisao** (hipoteses e efeitos), **foro/arbitragem** (passo 1).
15. **Assinaturas + 2 testemunhas.**

### 3. Titulo executivo (CPC 784 III) — desenhar para executar
Verbatim CPC 784: *"Sao titulos executivos extrajudiciais: [...] III - o documento particular assinado pelo devedor e por 2 (duas) testemunhas"*. O contrato assinado pelo franqueado **+ 2 testemunhas** e titulo executivo. **§4o:** em assinatura eletronica com integridade conferida pelo provedor, **dispensam-se as testemunhas**. As verbas liquidas (royalties/fundo/multa fixos) viram base de `execucao-contrato-franquia`. **Cadeia DRE -> COF -> contrato -> titulo: mesma base em todos.**

### 4. Natureza empresarial (sem CDC) — afirmar na minuta
Consignar a natureza **empresarial e paritaria** (art. 1o, *"sem caracterizar relacao de consumo ou vinculo empregaticio"*; STJ REsp 1.602.076/SP, 632.958/AL ✅). Efeitos: foro de eleicao valido, sem inversao do onus, sem hipossuficiencia. **Distincao critica:** a rede responde **perante o consumidor final** (CDC 14/18 — STJ REsp 1.426.578/SP ✅); isso e outro eixo, fora do contrato franqueador x franqueado.

## Entrega obrigatoria final
- Contrato redigido bloco a bloco, com taxas coerentes ao DRE/COF, restritivas remetidas a skill propria, foro/arbitragem definido pela gestao, e clausula de assinatura com 2 testemunhas (ou e-assinatura §4o) para titulo executivo.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. Foro/arbitragem SEMPRE pela `competencia-foro-arbitragem-franquia` antes de fechar. Bases financeiras so do `dre-unidade-modelo`. NUNCA citar a Lei 8.955/94 como vigente (revogada — art. 9o). Entrega fecha pela `suprema-corte-franchising`. Cross-link, nao duplicar: marca -> `marca-inpi-adv-os`; calculo de debito -> `calculosjudiciais-adv-os`/`execucao-adv-os`.
