# DRE da Unidade-Modelo + Modelagem Financeira da Franquia

> **Para:** skill `dre-unidade-modelo` (C2 Formatação) + insumo de `circular-oferta-franquia` (COF) e `contrato-de-franquia`.
> **O que é:** o DRE da unidade-modelo é o **reflexo financeiro da unidade que será comercializada** — o "modelo de negócio vendido". Dá segurança ao franqueado (qual o retorno esperado?) e ao franqueador (a unidade-piloto é lucrativa e *replicável*?), e alimenta as informações financeiras da **COF (art. 2º, Lei 13.966/2019)**.
> **Fronteira (não duplicar):** `cfo-combativo-os` (modelagem financeira pesada da rede inteira) · `calculosjudiciais-adv-os` / `execucao-adv-os` (memória de cálculo de débitos em execução). Aqui é só o **DRE do modelo de unidade**, não a contabilidade da franqueadora.

---

## 0. PRINCÍPIO ANTI-HALUCINAÇÃO (R-FRANQUIA no financeiro)

**O plugin ESTRUTURA o modelo; ele NÃO inventa os números.**

1. **Nunca cravar faturamento, CMV, aluguel, folha ou qualquer valor inventado.** Esses números são do **operador real** (o franqueador, a partir da unidade-piloto/própria). O plugin **pede** os dados e só monta a planilha/DRE sobre o que recebeu. Sem o dado, a célula fica **vazia + nota "preencher com dado real da unidade-piloto"** — jamais um número fabricado com cara de preciso.
2. **Benchmarks de mercado são referência 🟡** — variam por segmento, marca, praça, porte e ano. Servem de *régua de sanidade* ("seu CMV de 50% destoa da faixa 28–35% do food service — confirme"), **nunca** como substituto do dado real, **nunca** como promessa, e **nunca** como norma legal.
3. **Projeção ≠ promessa de resultado.** O DRE da unidade-modelo é cenário, não garantia. A franqueadora **não pode garantir lucro** (ver §5). Isso é compliance da COF e blindagem contra litígio futuro.
4. **A lei NÃO fixa percentuais** de royalties nem de fundo — só exige que a COF os **declare** com base de cálculo e finalidade (art. 2º IX). Os percentuais usados são os **reais do operador**, não os de tabela de mercado.

---

## 1. ESTRUTURA DO DRE DA UNIDADE-MODELO (linha a linha)

O DRE para franquias é uma **DRE projetada** (forward-looking), montada sobre **cenários futuros** considerando investimento, taxas da rede e projeção de receita — não a DRE contábil histórica.

### 1.1 Cascata canônica (do faturamento ao resultado da unidade)

| # | Linha | O que entra |
|---|-------|-------------|
| 1 | **(=) Faturamento bruto projetado** | Receita de vendas da unidade (ticket médio × volume, ou projeção mensal). **Dado do operador.** |
| 2 | **(−) Deduções sobre vendas** | Impostos sobre faturamento (Simples/ICMS/ISS/PIS/COFINS conforme regime), devoluções, cancelamentos |
| 3 | **(=) Receita líquida** | (1) − (2) |
| 4 | **(−) CMV / CPV / CSP** | Custo da mercadoria/produto vendido ou do serviço prestado. **Indicador-chave de previsibilidade da unidade.** |
| 5 | **(=) Margem bruta / de contribuição** | (3) − (4). Quanto cada R$ de venda sobra para cobrir o custo fixo |
| 6 | **(−) Despesas operacionais fixas** | Aluguel · folha + encargos · **pró-labore do franqueado** · energia/água · marketing local · contabilidade · software/taxa de sistema · manutenção |
| 7 | **(−) Royalties** | **% sobre o faturamento bruto** pago à franqueadora (uso de marca + know-how) |
| 8 | **(−) Fundo de marketing / propaganda** | **% sobre o faturamento bruto** destinado à publicidade institucional da rede |
| 9 | **(=) EBITDA (Lajida)** | Resultado operacional antes de juros, IR, depreciação e amortização |
| 10 | **(−) Depreciação / amortização** | Desgaste de equipamentos, obra, sistema (não é saída de caixa, mas entra no resultado) |
| 11 | **(−) Resultado financeiro / IRPJ-CSLL** | Juros do financiamento do investimento + tributos sobre lucro (se lucro real/presumido) |
| 12 | **(=) Resultado líquido da unidade** | O lucro que sobra para o franqueado — **depois** de remunerar o trabalho dele (pró-labore já na linha 6) |

> **Cuidado de modelagem (explicitar com o operador):** o **pró-labore do franqueado** (salário do dono que opera) entra como **despesa (linha 6)**. Se omitido, o "lucro" fica inflado e o DRE mente. A unidade tem de gerar lucro suficiente para cobrir todos os custos operacionais (**incluindo o salário do franqueado**) e ainda sobrar lucro líquido atraente.

### 1.2 Base de cálculo — onde royalties e fundo incidem

**Fato-âncora financeiro/contratual:** no modelo mais comum, royalties e fundo de marketing incidem **sobre o FATURAMENTO BRUTO mensal** (linha 1), **não** sobre o lucro. Variações possíveis (todas conforme o contrato/COF, não presumir):
- **% sobre faturamento bruto** — padrão de franquias de serviço/varejo.
- **% sobre compras** — quando o franqueador é o **fabricante** (royalty embutido no produto vendido ao franqueado).
- **valor fixo mensal** — alternativa para fundo/royalty em algumas redes.
- **% sobre lucro líquido** — existe, porém menos comum.

> **Por que importa para o contrato e a execução:** a **base de cálculo** definida no DRE/COF é a **mesma** que vai para a cláusula de royalties/fundo do contrato — e é o que se executa em `execucao-royalties` / `execucao-fundo-marketing`. Se o DRE diz "5% do faturamento bruto", o contrato e o título executivo têm de dizer o mesmo. **Coerência DRE ⇄ COF (IX) ⇄ contrato ⇄ título é anti-litígio.**

### 1.3 Mecânica ilustrativa (esqueleto — NÃO são valores reais)

Apenas para mostrar **como a cascata fecha** (percentuais e valores são placeholders a substituir pelos do operador):

```
Faturamento bruto mensal ......................... R$ [dado do operador]
(−) Royalties ......... [% do contrato] ........... R$ [calcular]
(−) Fundo de marketing  [% do contrato] ........... R$ [calcular]
(−) Demais despesas operacionais
     (aluguel, mercadoria/CMV, folha + pró-labore,
      impostos, energia, software) ............... R$ [dado do operador]
(=) Resultado líquido da unidade .................. R$ [resultado]   → margem líquida = resultado / faturamento
```

> A margem líquida resultante é **consequência dos números reais**, nunca um alvo cravado pela skill.

---

## 2. INVESTIMENTO INICIAL — composição e como estimar

**Metodologia canônica (Sebrae):** o investimento total é a soma de **três blocos**.

```
INVESTIMENTO TOTAL = Investimento fixo + Investimento pré-operacional + Capital de giro
```

| Bloco | O que compõe (no contexto de franquia) |
|-------|-----------------------------------------|
| **Investimento fixo** | Obra/reforma para padrão visual · arquitetura/leiaute (memorial — COF XIII-h) · equipamentos e máquinas · móveis e utensílios · estoque inicial · software/PDV · veículo (se aplicável) |
| **Investimento pré-operacional** | **Taxa inicial de franquia** · constituição da PJ (CNPJ, contrato social) · alvarás (sanitário, bombeiros, funcionamento) · registro de marca · treinamento inicial da equipe · honorários (contador/advogado) · marketing de inauguração |
| **Capital de giro** | Caixa para sustentar a unidade **até o faturamento estabilizar** — folha, pró-labore, fornecedores, aluguel, água/luz/internet, impostos dos primeiros meses |

**Recomendações de estimativa:**
- **Reserva de contingência:** manter ~**5% do capital de giro** como colchão para imprevistos (referência 🟡).
- **Taxa de franquia** entra no **pré-operacional**, é **valor fixo, único**, pago na assinatura (concessão de uso da marca + treinamento + suporte de implantação) e deve estar discriminada na COF (VIII-b).
- **Benchmarking de mercado** apenas como régua de sanidade da estrutura de custos (🟡).

> **Mapeamento direto para a COF (art. 2º VIII):** investimento fixo + pré-operacional + capital de giro = **VIII-a** (total estimado do investimento inicial); a taxa de franquia isolada = **VIII-b**; instalações/equipamentos/estoque inicial + condições de pagamento = **VIII-c**.

---

## 3. INDICADORES QUE O MODELO DEVE GERAR (com fórmulas)

O DRE projetado + o investimento inicial alimentam os indicadores de viabilidade.

### 3.1 Payback (prazo de retorno)
```
Payback (simples) = Investimento inicial / Ganho líquido no período
```
- **Payback simples:** soma os fluxos de caixa até igualar o investimento — ignora o valor do dinheiro no tempo.
- **Payback descontado:** desconta o fluxo por uma **TMA (Taxa Mínima de Atratividade)** via **VPL** — mais realista. Componentes da TMA: custo de oportunidade (ex.: Selic), risco do projeto, liquidez.
- **Régua de mercado 🟡:** payback **ideal < 36 meses** no cenário realista; acima disso a franquia perde atratividade.

### 3.2 TIR (Taxa Interna de Retorno)
Taxa de desconto que zera o VPL do fluxo de caixa projetado. Compara-se com a **TMA**: **TIR > TMA ⇒ projeto atrativo**. O plugin **calcula sobre o fluxo real do operador**, nunca arbitra uma TIR.

### 3.3 Ponto de equilíbrio (break-even)
```
PE em unidades   = Custos fixos / Margem de contribuição unitária
   onde  Margem de contribuição unitária = Preço de venda unit. − Custo variável unit.
PE em faturamento = PE em unidades × Preço de venda unitário
```
É o **faturamento mínimo mensal** que cobre todos os custos — abaixo dele, prejuízo; acima, lucro.
- **Régua de mercado 🟡:** break-even idealmente em **até ~6 meses** de operação.
- **Break-even ≠ payback:** break-even = volume de vendas para não ter prejuízo (recorrente/mensal); payback = tempo para recuperar o investimento inicial.

### 3.4 Margem líquida
```
Margem líquida (%) = Resultado líquido da unidade / Faturamento bruto × 100
```

### 3.5 ROI (Retorno sobre Investimento)
```
ROI (%) = (Ganho do investimento − Custo do investimento) / Custo do investimento × 100
```
KPI relacionado ao payback; ROI longo (>36 meses de retorno) torna a franquia menos competitiva (régua 🟡).

---

## 4. FAIXAS DE BENCHMARK DE MERCADO (referência 🟡 — NÃO são lei)

> ⚠️ A **Lei 13.966/2019 NÃO fixa percentuais** de royalties nem de fundo — só exige que a COF os **declare** com base de cálculo e finalidade (art. 2º IX). Os números abaixo são **prática de mercado**: servem de régua de sanidade, **não de norma**. **O plugin usa o % real do operador.**

### 4.1 Taxas típicas no Brasil (🟡 referência)

| Taxa | Natureza | Faixa usual de mercado 🟡 |
|------|----------|----------------------------|
| **Taxa inicial de franquia** | valor **fixo, único**, na assinatura | método "número mágico" ≈ 10% do investimento total da unidade; ou por valor de marca / concorrência |
| **Royalties** (serviço/varejo) | **% do faturamento bruto/mês** | **4% a 10%** |
| **Royalties** (franqueador = fabricante) | **% sobre as compras/mês** | **20% a 40%** |
| **Fundo de propaganda/marketing** | **% do faturamento bruto** ou valor fixo | **2% a 5%** |
| **Taxa de sistema** (opcional) | fixa ou variável (software/tecnologia) | não universal |
| **Taxa de renovação** | na prorrogação do contrato | ~igual à 1ª vigência + correção |

> **Nota jurídica sobre o fundo:** a lei **não estabelece limite** para a cobrança do fundo; exige apenas transparência sobre o que é cobrado, e o franqueado tem direito à **prestação de contas** do uso do fundo. O fundo é **verba afetada a marketing da rede** (dos franqueados, sob administração do franqueador), **não receita livre** da franqueadora. (Ver `jurisprudencia-franquia.md`, Tema E — cobrança do fundo condicionada à prestação de contas.)

### 4.2 Régua de viabilidade por segmento (🟡 — usar SÓ como sanidade)

| Segmento | Investimento médio | Custo/CMV | Margem líquida | Payback | Royalties |
|----------|--------------------|-----------|----------------|---------|-----------|
| **Alimentação / food service** | R$ 150k–500k | food cost 28%–35% | 10%–18% | 18–36 meses | 4%–6% |
| **Serviços** | R$ 50k–200k | custo op. 30%–45% | 15%–30% | 12–24 meses | 5%–10% |
| **Saúde e bem-estar** | R$ 100k–400k | custo prod. 15%–25% | 12%–22% | 18–30 meses | 5%–8% |

> Todos os valores acima são **referência de mercado 🟡**, capturados de fontes setoriais. Use para checar se o número do operador faz sentido — nunca como projeção a apresentar.

---

## 5. PREMISSAS E DISCLAIMERS (o que pode e o que NÃO pode ser dito)

### 5.1 Três cenários obrigatórios
Toda DRE de unidade-modelo profissional vem em **3 cenários**:
- **Otimista** — faturamento acima da média do segmento, custos controlados.
- **Realista (base)** — médias do segmento; é onde o payback deve ficar < 36 meses.
- **Conservador / pessimista** — faturamento abaixo, custos acima; teste de stress.

Acompanhar de **análise de sensibilidade** ("o que acontece se o faturamento cair 20%? se o aluguel subir?") — o break-even é sensível a variações de custo fixo/variável.

### 5.2 Projeção NÃO é promessa — limite da COF
- A franqueadora **NÃO pode garantir lucro nem retorno**. O DRE é **estimativa/cenário**, apresentado para **gestão de expectativas** — apresentar dados de forma transparente reduz a chance de litígio.
- As demonstrações financeiras servem de **base ética e legal** para *comprovar* projeções — mas comprovação de base **não é garantia** de resultado.
- **Texto-padrão de disclaimer** (a skill deve inserir): *"As projeções constantes deste DRE da unidade-modelo são estimativas baseadas em premissas e no desempenho de unidade(s) existente(s), NÃO constituindo promessa, garantia ou compromisso de faturamento, lucro ou retorno. Resultados reais dependem de gestão, ponto, praça, equipe e mercado, e podem divergir significativamente."*
- **Anti-CDC:** o contrato de franquia **não é relação de consumo** (art. 1º). Logo, o DRE não se rege pela lógica consumerista de "publicidade que vincula/oferta" — **mas informação falsa/omitida na COF** gera anulabilidade/nulidade + devolução corrigida (art. 2º §2º / art. 4º). **Mentir no DRE da COF é sanção dura.**

### 5.3 O que o operador precisa entregar (checklist do plugin)
Antes de montar o DRE, a skill pede ao franqueador, **da unidade-piloto/própria real**: faturamento mensal histórico, ticket médio e volume, CMV/CPV, aluguel, folha + encargos + pró-labore, energia/água, marketing local, regime tributário, **% de royalties e de fundo** que pretende cobrar, e a composição do investimento (fixo/pré-op/giro). Sem isso → **não há DRE; há só o esqueleto vazio.**

---

## 6. COMO O DRE SE CONECTA À COF E AO CONTRATO

### 6.1 Incisos do art. 2º (Lei 13.966/2019) que o DRE/modelagem alimenta

| Inciso COF | Conteúdo | O que o DRE/modelagem fornece |
|------------|----------|-------------------------------|
| **III** | Balanços e demonstrações da **franqueadora** (2 últimos exercícios) | *Contexto* — é da franqueadora, não da unidade; sustenta a credibilidade do modelo |
| **VIII-a** | Total estimado do **investimento inicial** | = investimento fixo + pré-operacional + capital de giro (§2) |
| **VIII-b** | Valor da **taxa inicial de franquia** | linha do pré-operacional, isolada |
| **VIII-c** | **Instalações, equipamentos, estoque inicial** + condições de pagamento | detalhamento do investimento fixo |
| **IX-a** | **Royalties** (remuneração periódica), com **base de cálculo** e finalidade | linha 7 do DRE + a base (% do faturamento bruto) |
| **IX-b** | Aluguel de equipamentos / ponto comercial | despesa operacional / pré-op (sublocação → art. 3º) |
| **IX-c** | **Taxa de publicidade / fundo de marketing** | linha 8 do DRE + base de cálculo |
| **IX-d** | **Seguro mínimo** | despesa operacional fixa |
| **XVIII** | Penalidades, multas, indenizações e valores | não é DRE, mas a **multa** é o que se executa no contencioso |

> **Regra de ouro:** os valores de **VIII** e **IX** da COF têm de **bater** com as linhas do DRE da unidade-modelo. Incoerência entre o DRE apresentado e a COF é exatamente o tipo de "informação falsa/omitida" que dispara o art. 2º §2º / art. 4º.

### 6.2 Conexão com o contrato de franquia
- A **base de cálculo** dos royalties (IX-a) e do fundo (IX-c) definida no DRE/COF é **transcrita** para as cláusulas financeiras do contrato (`contrato-de-franquia`): **mesma base, mesmo percentual, mesma periodicidade**.
- Essa mesma base vira **título/parâmetro de execução** na inadimplência (`execucao-royalties`, `execucao-fundo-marketing`, `execucao-debitos-franquia`, `execucao-multa`). **DRE → COF → contrato → título** é uma cadeia única; quebrá-la em qualquer elo abre flanco.
- O DRE **baliza o teto de taxas**: elas têm de sustentar a franqueadora **sem inviabilizar** a lucratividade do franqueado — o DRE mostra o limite máximo de despesas que a unidade franqueada pode suportar.

---

## 7. SÍNTESE DE FATOS-ÂNCORA (para o plugin)

| # | Fato | Marca |
|---|------|-------|
| 1 | DRE da unidade-modelo é **projetada** (cenários futuros), não a DRE contábil histórica | ✅ |
| 2 | Cascata: faturamento → deduções → receita líq. → CMV → margem → desp. op. → **royalties** → **fundo** → EBITDA → deprec. → resultado líq. | ✅ |
| 3 | Royalties e fundo incidem **sobre o faturamento bruto** (modelo padrão); a base do DRE = a do contrato e do título | ✅ |
| 4 | Pró-labore do franqueado **é despesa** (linha 6); omiti-lo infla o lucro | ✅ |
| 5 | Investimento total = **fixo + pré-operacional + capital de giro** | ✅ |
| 6 | Payback = investimento / ganho no período; break-even = custos fixos / margem de contribuição unitária | ✅ fórmulas |
| 7 | Réguas (payback < 36m, break-even ~6m, faixas de %, "número mágico" 10%) são **referência de mercado** | 🟡 |
| 8 | A **lei não fixa nem limita** percentuais de royalties/fundo — só exige declaração (IX) + prestação de contas do fundo | ✅ |
| 9 | DRE em **3 cenários** (otimista/realista/conservador) + sensibilidade | ✅ |
| 10 | Projeção **NÃO é promessa**; franqueadora **não garante lucro**; informação falsa na COF → anulabilidade + devolução (art. 2º §2º/art. 4º) | ✅ |
| 11 | DRE alimenta a COF: **VIII-a/b/c + IX-a/b/c/d**; coerência DRE⇄COF⇄contrato⇄título é anti-litígio | ✅ |

---

*O DRE da unidade-modelo é estrutura + disciplina anti-halucinação: o plugin monta a cascata e calcula os indicadores SOBRE os números reais do operador; benchmarks de mercado entram só como régua 🟡; nada de faturamento inventado; projeção nunca vira promessa de lucro.*
