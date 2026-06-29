---
name: dre-unidade-modelo
description: "Modela o reflexo financeiro da unidade comercializada (o modelo de negocio vendido) — cascata faturamento -> deducoes -> CMV -> despesas -> royalties -> fundo -> EBITDA -> resultado liquido; investimento inicial (fixo + pre-operacional + giro); payback, break-even, ROI/TIR; 3 cenarios + sensibilidade. NUNCA crava numero inventado: pede os dados reais do operador; benchmark de mercado e regua 🟡, nunca promessa; projecao != promessa de lucro (disclaimer obrigatorio). Alimenta a COF (art. 2o VIII/IX da Lei 13.966/2019) e a base de calculo (faturamento bruto) do contrato. Use quando o operador disser DRE da unidade-modelo, modelar a viabilidade financeira da franquia, projecao de faturamento/payback da unidade, investimento inicial da franquia, ou base de calculo de royalties/fundo."
---

# DRE-UNIDADE-MODELO

> Camada 2 — Formatacao da franquia. Modela o **reflexo financeiro da unidade que sera comercializada** (o "modelo vendido"). Alimenta a COF (art. 2o VIII/IX) e a base de calculo do `contrato-de-franquia`. **Estrutura o modelo; NAO inventa os numeros.**

## Anexos obrigatorios (context/)
- `context/financeiro-dre.md` — **toda** a cascata (§1), investimento inicial (§2), indicadores/formulas (§3), benchmarks 🟡 (§4), disclaimers (§5), conexao COF/contrato (§6) — **grep + ler a faixa**.
- `context/lei-13966-2019.md` — **art. 2o VIII** (a/b/c investimento e taxa), **IX** (a/b/c/d royalties/aluguel/fundo/seguro), §2o / **art. 4o** (COF falsa/omissa -> anulabilidade + devolucao).

## Objetivo
Montar a **DRE projetada** da unidade-modelo + o investimento inicial + os indicadores de viabilidade **sobre os numeros reais do operador**, de modo que a COF (VIII/IX) e o contrato fiquem **coerentes** com o modelo — sem cravar valor inventado e sem transformar projecao em promessa de lucro.

## Quando ativar
- O franqueador precisa do DRE/viabilidade da unidade-piloto para formatar a franquia.
- Faltam os numeros financeiros que a COF (VIII/IX) e o contrato (royalties/fundo) exigem.
- Validar a coerencia financeira entre DRE, COF e contrato.

## Metodologia

### 0. Principio anti-halucinacao (R-FRANQUIA financeiro) — antes de tudo
**O plugin ESTRUTURA o modelo; NAO inventa numeros.** Nunca cravar faturamento, CMV, aluguel, folha ou percentuais inventados — sao do **operador real** (unidade-piloto/propria). Sem o dado, a celula fica **vazia + nota "preencher com dado real da unidade-piloto"**, jamais um numero fabricado com cara de preciso. Benchmark de mercado e **regua 🟡** (sanidade), nunca substituto do dado real, nunca promessa, nunca norma legal. **A lei NAO fixa percentuais** de royalties/fundo (so exige declara-los — art. 2o IX).

### 1. Coletar os dados reais do operador (checklist — §5.3)
Pedir da unidade-piloto/propria: faturamento mensal historico, ticket medio e volume, CMV/CPV, aluguel, folha + encargos + **pro-labore**, energia/agua, marketing local, regime tributario, **% de royalties e de fundo** pretendidos, e a composicao do investimento (fixo/pre-op/giro). **Sem isso -> nao ha DRE; ha so o esqueleto vazio.**

### 2. Montar a cascata canonica (§1.1)
Faturamento bruto projetado -> (-) deducoes sobre vendas -> (=) receita liquida -> (-) **CMV/CPV/CSP** -> (=) margem bruta/contribuicao -> (-) despesas operacionais fixas (aluguel, folha, **pro-labore do franqueado**, energia, marketing local, contabilidade, software) -> (-) **royalties** -> (-) **fundo de marketing** -> (=) **EBITDA** -> (-) depreciacao/amortizacao -> (-) resultado financeiro/IRPJ-CSLL -> (=) **resultado liquido da unidade**.
> **Cuidado de modelagem (explicitar):** o **pro-labore do franqueado** entra como **despesa (linha 6)**. Omiti-lo infla o "lucro" e o DRE mente — a unidade tem de cobrir todos os custos **incluindo o salario do dono** e ainda sobrar lucro liquido.

### 3. Base de calculo de royalties e fundo (§1.2) — amarra ao contrato
No modelo padrao, royalties e fundo incidem **sobre o FATURAMENTO BRUTO mensal**, nao sobre o lucro. Variacoes (so conforme contrato/COF, nunca presumir): % sobre compras (franqueador fabricante), valor fixo mensal, % sobre lucro liquido. **A base definida aqui e a MESMA que vai para a clausula de royalties/fundo do contrato e para o titulo executivo.** Se o DRE diz "5% do faturamento bruto", contrato e titulo dizem o mesmo. **Coerencia DRE <-> COF (IX) <-> contrato <-> titulo e anti-litigio.**

### 4. Investimento inicial (§2)
**INVESTIMENTO TOTAL = Investimento fixo + Investimento pre-operacional + Capital de giro.**
- **Fixo:** obra/reforma do padrao visual, arquitetura/leiaute (memorial — COF XIII-h), equipamentos, moveis, estoque inicial, software/PDV.
- **Pre-operacional:** **taxa inicial de franquia** (fixa, unica), constituicao da PJ, alvaras, registro de marca, treinamento, honorarios, marketing de inauguracao.
- **Capital de giro:** caixa ate o faturamento estabilizar (folha, pro-labore, fornecedores, aluguel, impostos dos primeiros meses). Reserva de contingencia ~5% do giro (🟡).
- **Mapa COF:** fixo+pre-op+giro = **VIII-a**; taxa de franquia isolada = **VIII-b**; instalacoes/equipamentos/estoque + condicoes de pagamento = **VIII-c**.

### 5. Indicadores de viabilidade (§3 — formulas)
- **Payback (simples)** = Investimento inicial / Ganho liquido no periodo. (Descontado usa TMA/VPL.) Regua 🟡: ideal < 36 meses.
- **Break-even (PE em unidades)** = Custos fixos / Margem de contribuicao unitaria; **PE em faturamento** = PE unidades x Preco unitario. Regua 🟡: ~6 meses. (Break-even != payback.)
- **Margem liquida (%)** = Resultado liquido / Faturamento bruto x 100.
- **ROI (%)** = (Ganho - Custo do investimento) / Custo do investimento x 100. **TIR** vs TMA (TIR > TMA = atrativo). Calcular **sobre o fluxo real do operador**, nunca arbitrar.

### 6. Tres cenarios + sensibilidade + disclaimer (§5)
- Apresentar em **3 cenarios**: otimista, **realista (base)** (onde o payback deve ficar < 36m), conservador/pessimista (stress) + analise de sensibilidade ("e se o faturamento cair 20%? se o aluguel subir?").
- **Projecao != promessa.** A franqueadora **NAO pode garantir lucro nem retorno**. Inserir o disclaimer verbatim (§5.2): *"As projecoes constantes deste DRE da unidade-modelo sao estimativas baseadas em premissas e no desempenho de unidade(s) existente(s), NAO constituindo promessa, garantia ou compromisso de faturamento, lucro ou retorno. Resultados reais dependem de gestao, ponto, praca, equipe e mercado, e podem divergir significativamente."*
- **Anti-CDC, mas atencao:** franqueador x franqueado **nao e relacao de consumo** (art. 1o) — o DRE nao se rege pela logica de "oferta que vincula"; **porem informacao falsa/omitida na COF** gera anulabilidade/nulidade + devolucao corrigida (art. 2o §2o / art. 4o). **Mentir no DRE da COF e sancao dura.**

### 7. Conexao COF/contrato (§6 — regra de ouro)
Os valores de **VIII** e **IX** da COF tem de **bater** com as linhas do DRE; a base dos royalties/fundo e transcrita para o contrato e vira parametro de execucao. Incoerencia DRE <-> COF e exatamente o tipo de "informacao falsa/omitida" que dispara o art. 2o §2o / art. 4o.

## Entrega obrigatoria final
- DRE projetado (cascata) em 3 cenarios + investimento inicial mapeado para VIII-a/b/c + indicadores (payback/break-even/margem/ROI) + disclaimer obrigatorio + nota de coerencia com COF (IX) e contrato. Celulas sem dado real ficam **marcadas como pendencia**, nunca preenchidas com numero inventado.

## Guard
Nenhum numero inventado — so dados reais do operador; benchmark 🟡 e regua, nao projecao. Disclaimer obrigatorio em todo DRE. A lei NAO fixa percentuais (art. 2o IX so exige declarar). Dispositivos pela `validador-franquia`; entrega fecha pela `suprema-corte-franchising`. Cross-link, nao duplicar: modelagem financeira pesada da rede -> `cfo-combativo-os`; memoria de calculo de debito em execucao -> `calculosjudiciais-adv-os`/`execucao-adv-os`. Alimenta `circular-oferta-franquia` (VIII/IX) e `contrato-de-franquia` (base de calculo).
