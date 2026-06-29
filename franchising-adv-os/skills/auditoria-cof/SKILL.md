---
name: auditoria-cof
description: "DIFERENCIAL DEFENSIVO (lado FRANQUEADO): audita a COF de TERCEIRO ANTES de o franqueado assinar — checklist inciso a inciso dos 23 incisos do art. 2o da Lei 13.966/2019 apontando o que falta, esta omisso, vago ou aparenta ser falso; confere o prazo de entrega >= 10 dias (§1o); e sinaliza cada deficiencia que gera ANULABILIDADE/NULIDADE + devolucao de royalties/filiacao corrigida (§2o / art. 4o) — ou seja, ALAVANCAGEM negocial e municao pre-constituida do franqueado. Espelho de `circular-oferta-franquia` (que monta; esta audita). Liga a `acao-anulatoria-cof` quando o vicio ja se consumou. Use quando o operador disser meu cliente vai comprar uma franquia, auditar a COF, conferir a circular antes de assinar, analisar a COF que recebi, a franqueadora me entregou a circular, vale a pena assinar esse contrato de franquia."
---

# AUDITORIA-COF

> Consultivo (diferencial — defensivo). **Lado: franqueado/candidato** que recebeu a COF de terceiro e ainda **nao assinou**. Espelho de `circular-oferta-franquia`: aquela monta a COF (lado franqueador); esta **caca deficiencias** (lado franqueado). Cada falha vira alavancagem.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2o (23 incisos I a XXIII)**, **§1o (prazo de 10 dias)**, **§2o (sancao)**, **art. 4o (COF omissa/falsa)** — a regua da auditoria. `grep -niE "art. 2|§1|§2|art. 4|inciso" context/lei-13966-2019.md`.
- `context/jurisprudencia-franquia.md` — **Tema E** (COF < 10 dias / omissa / falsa -> anulacao + devolucao; exige prejuizo + tempo razoavel; execucao prolongada convalida) — so apos confirmar.
- `context/financeiro-dre.md` — incisos **VIII/IX**: conferir se os numeros financeiros estao completos e coerentes (ou se ha promessa de lucro disfarçada).
- `context/manuais-estrutura.md` — **XIII-f/h, XIV**: a COF promete manuais/padrao/marca que existem?

## Objetivo
Produzir um **laudo de auditoria** da COF recebida: o que cumpre, o que falta/omite/vagueia/aparenta falso (inciso a inciso), o status do prazo de 10 dias, e o **mapa de alavancagem** (quais deficiencias autorizam anulabilidade + devolucao). Decisao informada: assinar, exigir correcoes, ou nao assinar.

## Quando ativar
- O cliente e candidato a franqueado e recebeu a COF; ainda nao assinou (ou assinou ha pouco e quer avaliar).
- Gatilhos: "auditar a COF", "conferir a circular antes de assinar", "recebi a COF da franqueadora", "vale a pena assinar essa franquia?".

## Metodologia

### 1. Status do prazo de 10 dias (art. 2o §1o) — a falha mais comum
> **Art. 2o §1o** — a COF deve ser entregue **no minimo 10 dias antes** da assinatura do contrato/pre-contrato ou do **pagamento de qualquer taxa**.

Datar a entrega vs a data prevista de assinatura/pagamento. **Menos de 10 dias = vicio** que abre a sancao do §2o. Orientar o cliente a **nao pagar nem assinar** antes de fechar os 10 dias (preserva a alavancagem).

### 2. Checklist dos 23 incisos (art. 2o) — caca a deficiencias
Para cada inciso, classificar: **OK / vago / omisso / aparente falso**. Pontos de maior risco:
- **III** — balancos da franqueadora dos **2 ultimos exercicios** presentes? (omissao recorrente).
- **IV** — **acoes judiciais relativas a franquia** declaradas? Omitir litigio relevante = anulacao (Tema E 🟡). Cruzar com `due-diligence-rede-franquia`.
- **VIII/IX** — investimento, taxa de franquia, **royalties/fundo com base de calculo e finalidade** completos e coerentes? Numero faltante/disfarce de promessa de lucro = bandeira vermelha (financeiro-dre).
- **X** — relacao completa de franqueados **+ desligados nos ultimos 24 meses**? (sinal de saude da rede — liga a due-diligence).
- **XI** — politica territorial/exclusividade clara?
- **XIII** — suporte/supervisao/treinamento/**manuais (f)**/ **padrao arquitetonico (h)** descritos com lastro real?
- **XIV** — **situacao da marca/PI** (registro/pedido, classe) — a franqueadora e titular/requerente (art. 1o §1o)? (cross-link `marca-inpi-adv-os`).
- **XV/XXI** — **nao-concorrencia** pos-contratual e na vigencia com **limites** (territorio + prazo) — clausula aniquiladora da atividade tende a abusiva.
- **XVI/XVIII/XXII** — contrato-padrao anexo; penalidades/multas e valores; prazo e renovacao.

### 3. Coerencia e veracidade
Cruzar **COF x contrato-padrao (XVI) x numeros (VIII/IX)**. Incoerencia ou informacao que aparenta falsa dispara o **art. 4o** (COF que omite exigencia ou veicula informacao falsa -> mesma sancao do §2o + sancoes penais).

### 4. Mapa de alavancagem (a municao do franqueado)
> **Art. 2o §2o** — descumprido o §1o, o franqueado pode **arguir anulabilidade ou nulidade** e **exigir a devolucao** de filiacao e royalties **corrigidos monetariamente**. **Art. 4o** estende a COF omissa/falsa.

Listar cada deficiencia -> efeito juridico (anulabilidade + devolucao). **Atencao honesta (Tema E):** a anulacao exige **prejuizo comprovado + pedido em tempo razoavel**; **execucao prolongada convalida** e mero insucesso nao anula — a auditoria PRE-assinatura e a hora de ouro (vicio cristalino, sem convalidacao).

## Entrega obrigatoria final
- Laudo de auditoria da COF: status do prazo de 10 dias; tabela inciso-a-inciso (OK/vago/omisso/falso); coerencia COF x contrato x numeros; **mapa de alavancagem** (deficiencia -> anulabilidade/devolucao); recomendacao (assinar / exigir correcoes / nao assinar) + alerta sobre arbitragem no contrato-padrao.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. Tema E so apos `varredura-jurisprudencial-pre-tese` (e respeitando a ressalva honesta: prejuizo + tempo razoavel; convalidacao). Numeros so do que a COF traz — nao inventar. Se o vicio ja se consumou e o cliente quer litigar -> `acao-anulatoria-cof`. Saude da rede -> `due-diligence-rede-franquia`. Marca -> `marca-inpi-adv-os`. Entrega fecha pela `suprema-corte-franchising`.
