---
name: circular-oferta-franquia
description: "Monta a Circular de Oferta de Franquia (COF) com os 23 incisos obrigatorios do art. 2o da Lei 13.966/2019 — checklist inciso a inciso do que cada um exige; cuida do prazo de entrega >= 10 dias (§1o) e blinda contra anulabilidade/nulidade + devolucao de royalties/filiacao corrigida (§2o e art. 4o). Garante coerencia COF <-> DRE <-> contrato. Use quando o operador disser montar a COF, circular de oferta de franquia, documento pre-contratual da franquia, o que precisa ter na COF, vou entregar a circular ao candidato a franqueado, ou revisar/conferir a COF antes de entregar."
---

# CIRCULAR-OFERTA-FRANQUIA (COF)

> Camada 2 — Formatacao da franquia. Documento pre-contratual obrigatorio do franqueador. Lado: **franqueador** (montar a COF). Para auditar a COF de TERCEIRO antes de o franqueado assinar, ver `auditoria-cof`.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2o (23 incisos, I a XXIII)**, **§1o (prazo de 10 dias)**, **§2o (sancao)**, **art. 4o (COF omissa/falsa)**, art. 3o (sublocacao) — **grep + ler a faixa**.
- `context/financeiro-dre.md` — incisos **VIII** (investimento) e **IX** (royalties/fundo/seguro): os numeros vem do `dre-unidade-modelo`, nunca inventados.
- `context/manuais-estrutura.md` — incisos **XIII-f** (manuais), **XIII-h** (arquitetonico/memorial), **XIV** (marca).
- `context/jurisprudencia-franquia.md` — **Tema E** (so ✅): COF < 10 dias / omissa / falsa -> anulacao + devolucao corrigida.

## Objetivo
Montar a COF **completa, objetiva e em lingua portuguesa**, varrendo os 23 incisos do art. 2o um a um, com os valores batendo com o DRE da unidade-modelo e com o contrato — entregue no prazo legal para que NENHUM flanco de anulabilidade fique aberto (§2o / art. 4o). A COF e a vacina contra o litigio futuro do franqueado.

## Quando ativar
- O franqueador vai oferecer a franquia a um candidato e precisa do documento pre-contratual.
- Revisar/conferir uma COF antes de entregar (do lado de quem monta a rede).
- O contrato/DRE ja existe e falta consolidar a circular que os antecede.

## Metodologia

### 1. Checklist dos 23 incisos do art. 2o (montar inciso a inciso)
Para cada inciso, registrar o conteudo; o que ficar **sem dado real** vira pendencia explicita (jamais preencher com numero inventado — isso e o "informacao falsa" do art. 4o).

- **I** — historico resumido do negocio franqueado.
- **II** — qualificacao completa do franqueador e empresas ligadas, com **respectivos CNPJ**.
- **III** — **balancos e demonstracoes financeiras da franqueadora dos 2 ultimos exercicios** (e da franqueadora, nao da unidade; ver `dre-unidade-modelo` §6.1).
- **IV** — **acoes judiciais relativas a franquia** que questionem o sistema ou possam comprometer a operacao (franqueador, controladoras, subfranqueador, titulares de marca/PI). *(Omitir disclosure de litigio relevante = anulacao — Tema E ✅.)*
- **V** — descricao detalhada da franquia + descricao geral do negocio e atividades do franqueado.
- **VI** — perfil do franqueado ideal (experiencia, escolaridade, caracteristicas).
- **VII** — requisitos de envolvimento direto do franqueado na operacao/administracao.
- **VIII** — **a)** total estimado do investimento inicial; **b)** valor da **taxa inicial de filiacao/franquia**; **c)** instalacoes, equipamentos e estoque inicial + condicoes de pagamento. **(Puxa do `dre-unidade-modelo`: fixo + pre-operacional + giro = VIII-a.)**
- **IX** — taxas periodicas e outros valores, com **base de calculo e finalidade**: **a)** royalties; **b)** aluguel de equipamentos/ponto; **c)** **taxa de publicidade / fundo de marketing**; **d)** seguro minimo. **(Mesma base do DRE e do contrato.)**
- **X** — **relacao completa de todos os franqueados** + os que **se desligaram nos ultimos 24 meses** (nomes, enderecos, telefones).
- **XI** — politica territorial: exclusividade/preferencia; vendas fora do territorio; concorrencia entre unidades proprias e franqueadas.
- **XII** — obrigacao de adquirir de **fornecedores indicados/aprovados** + relacao completa.
- **XIII** — o que o franqueador oferece e condicoes: a) suporte; b) supervisao; c) servicos; d) inovacao tecnologica; e) treinamento (duracao/conteudo/custos); **f) manuais de franquia** *(lastro: `manual-de-operacoes`)*; g) auxilio na escolha do ponto; **h) leiaute e padroes arquitetonicos (arranjo fisico, memorial descritivo, composicao e croqui)** *(lastro: `manual-arquitetonico`)*.
- **XIV** — **situacao da marca** e PI: caracterizacao, no de registro/pedido, classe/subclasse *(cross-link `marca-inpi-adv-os`; lastro `manual-da-marca`)*.
- **XV** — situacao do franqueado **apos a expiracao do contrato** quanto a: **a)** know-how/segredos; **b)** **implantacao de atividade concorrente** *(base da nao-concorrencia pos-contratual)*.
- **XVI** — modelo do **contrato-padrao** (e pre-contrato), texto completo, anexos, prazos *(`contrato-de-franquia`)*.
- **XVII** — regras de **transferencia ou sucessao**, se houver.
- **XVIII** — situacoes de **penalidades, multas, indenizacoes** e valores estabelecidos no contrato.
- **XIX** — cotas minimas de compra + condicoes de recusa de produtos/servicos.
- **XX** — **conselho/associacao de franqueados** e competencias de **gestao/fiscalizacao de fundos** *(amarra com `prestacao-contas-fundo-marketing`)*.
- **XXI** — **regras de limitacao a concorrencia DURANTE a vigencia**, com **abrangencia territorial, prazo de vigencia da restricao e penalidades** *(base da `clausula-nao-concorrencia-e-bandeira`)*.
- **XXII** — **especificacao precisa do prazo contratual e condicoes de renovacao**, se houver.
- **XXIII** — local, dia e hora para recebimento/abertura de envelopes (orgao/entidade publica — so em licitacao).

### 2. Prazo de 10 dias (art. 2o §1o) — entrega blindada
Anexar **comprovante datado** de entrega. Verbatim: *"A COF devera ser entregue ao candidato no minimo 10 (dez) dias antes da assinatura do contrato ou pre-contrato, ou do pagamento de qualquer taxa ao franqueador ou pessoa ligada"* (salvo licitacao/pre-qualificacao publica). **Contar os 10 dias e protocolar a entrega** — sem prova de antecedencia, a sancao do §2o fica disponivel ao franqueado.

### 3. Blindagem contra anulabilidade (art. 2o §2o + art. 4o)
Verbatim §2o: *"o franqueado podera arguir anulabilidade ou nulidade, conforme o caso, e exigir a devolucao de todas e quaisquer quantias ja pagas ao franqueador ou a terceiros por este indicados, a titulo de filiacao ou de royalties, corrigidas monetariamente"*. Art. 4o estende a sancao a **COF que omite informacao exigida ou veicula informacao falsa** ("sem prejuizo das sancoes penais"). Logo: **nada omitido, nada falso, prazo cumprido**.

### 4. Coerencia COF <-> DRE <-> contrato (regra de ouro anti-litigio)
Os valores de **VIII** e **IX** tem de **bater** com as linhas do `dre-unidade-modelo` e com as clausulas financeiras do `contrato-de-franquia` (mesma base, mesmo percentual, mesma periodicidade). Incoerencia DRE/COF/contrato = exatamente o "informacao falsa/omitida" que dispara o art. 4o. **DRE -> COF -> contrato -> titulo e cadeia unica.**

### 5. Disclaimer financeiro (projecao nao e promessa)
Se a COF traz numeros de retorno, inserir o disclaimer do `dre-unidade-modelo` §5.2: projecao **nao** constitui promessa/garantia de faturamento ou lucro. A franqueadora **nao pode garantir lucro**. (Nao confundir com CDC: franqueador x franqueado **nao e relacao de consumo** — art. 1o; mas COF falsa gera anulabilidade.)

## Entrega obrigatoria final
- COF redigida com os 23 incisos preenchidos (ou pendencia marcada onde falta dado real), prazo de 10 dias com comprovante de entrega, contrato-padrao anexado (XVI), e checklist de coerencia com DRE e contrato.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` (cruza `context/`). Numeros financeiros so do `dre-unidade-modelo` (nunca inventar). Jurisprudencia (Tema E) so apos `varredura-jurisprudencial-pre-tese` confirmar ao vivo. Entrega fecha pela `suprema-corte-franchising`. Cross-link, nao duplicar: registro de marca -> `marca-inpi-adv-os`.
