---
name: base-legal-13966
description: "Recupera e explica os dispositivos da Lei 13.966/2019 (Lei de Franquia VIGENTE) sob demanda das demais skills do plugin. Localiza o artigo por grep em context/lei-13966-2019.md, traz texto verbatim + finalidade + efeito prático: COF (art. 2º, 23 incisos I-XXIII), prazo de 10 dias (§1º), sanção por descumprimento (§2º + art. 4º = anulabilidade/nulidade + devolução corrigida de filiação e royalties), contrato (art. 7º: português + lei BR; §1º arbitragem), sublocação (art. 3º), PI (art. 8º), revogação da 8.955/94 (art. 9º). Mapa de qual inciso/artigo para qual situação. Use quando precisar do texto vigente de um artigo da Lei de Franquia, ou ao perguntar qual artigo rege a COF/royalties/fundo/prazo, base legal da franquia, esse dispositivo está em vigor, fundamento na 13.966."
---

# BASE-LEGAL-13966 — Recuperador de dispositivos da Lei de Franquia

> Camada 1 (Fundação). Fonte de verdade da Lei 13.966/2019 para as demais skills. Não redige peça: entrega o dispositivo correto, vigente e explicado.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — Lei 13.966/2019 consolidada, verbatim do Planalto. **Localizar o artigo por grep e ler a faixa**, nunca despejar o anexo inteiro.
- `context/jurisprudencia-franquia.md` — quando precisar do julgado ✅ que sustenta o dispositivo.

## Objetivo
Devolver, para qualquer artigo/inciso/§ da Lei de Franquia: o **texto exato vigente**, a **finalidade**, o **efeito prático** e o **status de vigência** — sem reproduzir a lei inteira e sem inventar redação.

## Quando ativar
- Outra skill (COF, contrato, notificação, ação, recurso) precisa do dispositivo fundante da Lei 13.966.
- O operador pergunta qual artigo/inciso rege a COF, o prazo, royalties, fundo, arbitragem, sublocação.
- Há dúvida se um dispositivo está vigente (atenção à transição 8.955/94 → 13.966/2019).

## Metodologia

1. **Localizar por grep**, nunca abrir o anexo inteiro. O anexo titula `## Art. Nº`:
   - artigo conhecido: `grep -n "Art\. 2" context/lei-13966-2019.md`;
   - por tema: `grep -niE "royalt|fundo|prazo|arbitr|sublocac" context/lei-13966-2019.md`.
2. **Ler só a faixa** retornada com `Read offset/limit`. Copiar a redação **verbatim** — nunca parafrasear como se fosse a lei.

3. **STATUS DE VIGÊNCIA — não errar (art. 9º + 10):** a Lei 13.966/2019 **revogou a Lei 8.955/94** (art. 9º), em vigor desde ~26/03/2020. **NUNCA citar a 8.955/94 como vigente.** Acórdão antigo que aplica a 8.955 deve ser **mapeado** para o dispositivo equivalente da 13.966.

4. **Art. 1º — natureza (âncora anti-CDC).** Verbatim: *"...mediante remuneração direta ou indireta, **sem caracterizar relação de consumo ou vínculo empregatício** em relação ao franqueado ou a seus empregados, ainda que durante o período de treinamento."* Efeito: relação **empresarial/paritária**; CDC não incide entre franqueador e franqueado (detalhe em `natureza-empresarial-nao-cdc`); sem vínculo trabalhista.

5. **Art. 2º — COF (23 incisos I a XXIII).** Caput: a COF é **obrigatória**, *"escrita em língua portuguesa, de forma objetiva e acessível, contendo obrigatoriamente"* os 23 itens. **Mapa "qual inciso para qual situação":**

   | Situação / pedido | Inciso(s) art. 2º |
   |---|---|
   | Histórico do negócio | I |
   | Qualificação + CNPJ do franqueador e ligadas | II |
   | Balanços dos 2 últimos exercícios | III |
   | Ações judiciais sobre a franquia (due diligence) | IV |
   | Descrição da franquia e do negócio | V |
   | Perfil do franqueado ideal | VI |
   | Envolvimento direto do franqueado | VII |
   | Investimento inicial + taxa de filiação + instalações | VIII (a/b/c) |
   | Taxas periódicas: **royalties** (a), aluguel (b), **fundo de marketing/publicidade** (c), seguro (d) | IX |
   | Lista de franqueados + **desligados nos últimos 24 meses** | X |
   | Política territorial / exclusividade / concorrência entre unidades | XI |
   | Fornecedores indicados/aprovados | XII |
   | Suporte, supervisão, treinamento (e), **manuais** (f), **leiaute/padrões arquitetônicos/memorial** (h) | XIII |
   | Situação da **marca** e PI (nº registro/pedido, classe) | XIV |
   | Pós-contrato: know-how/segredos (a) + **atividade concorrente** (b) → base da não-concorrência | XV |
   | Modelo do contrato-padrão / pré-contrato | XVI |
   | Regras de **transferência/sucessão** | XVII |
   | Penalidades, multas, indenizações e valores | XVIII |
   | Cotas mínimas de compra | XIX |
   | Conselho/associação de franqueados + gestão de **fundos** | XX |
   | **Limitação à concorrência na vigência** (território + prazo + penalidade) | XXI |
   | Prazo contratual + condições de **renovação** | XXII |
   | Local/dia/hora de recebimento (licitação pública) | XXIII |

6. **Art. 2º §1º — PRAZO DE 10 DIAS.** Verbatim: a COF *"deverá ser entregue ao candidato **no mínimo 10 (dez) dias antes** da assinatura do contrato ou pré-contrato, ou do pagamento de qualquer taxa"* ao franqueador ou pessoa ligada (salvo licitação/pré-qualificação pública).

7. **Art. 2º §2º — SANÇÃO (âncora).** Verbatim: *"...o franqueado poderá **arguir anulabilidade ou nulidade**, conforme o caso, **e exigir a devolução de todas e quaisquer quantias já pagas** ao franqueador ou a terceiros por este indicados, a título de **filiação ou de royalties, corrigidas monetariamente**."* Aciona `acao-anulatoria-cof`.

8. **Art. 4º — COF omissa/falsa.** Quem *"omitir informações exigidas por lei ou veicular informações falsas"* na COF sofre a mesma sanção do art. 2º §2º (anulabilidade/nulidade + devolução corrigida), *"sem prejuízo das sanções penais cabíveis"*.

9. **Art. 3º — sublocação do ponto.** Qualquer das partes pode propor a renovação da locação; o aluguel pago pelo franqueado **pode ser superior** ao que o franqueador paga ao proprietário **desde que** (I) previsto na COF e no contrato e (II) sem onerosidade excessiva (equilíbrio econômico-financeiro).

10. **Art. 7º — contrato + arbitragem.** Inc. I: contrato com efeitos no território nacional = **escrito em língua portuguesa e regido pela legislação brasileira**. **§1º (âncora arbitragem):** *"As partes poderão eleger juízo arbitral para solução de controvérsias relacionadas ao contrato de franquia."* Detalhe processual em `competencia-foro-arbitragem-franquia`.

11. **Art. 8º — PI.** A aplicação da lei observa a legislação de **propriedade intelectual** vigente (LPI 9.279/96; cross-link `marca-inpi-adv-os`).

## Entrega obrigatoria final
Citação do dispositivo (artigo/§/inciso) com **texto verbatim** + finalidade + efeito prático + status de vigência + ponteiro do trecho do anexo lido. Em dúvida de redação/vigência, **sinalizar e mandar checar** — nunca preencher de memória.

## Guard
Nenhum dispositivo entregue sem confirmar a redação no anexo via grep. **Jamais citar a Lei 8.955/94 como vigente.** Citação cruzada por `validador-franquia`; toda peça que use isto fecha pela `suprema-corte-franchising`.
