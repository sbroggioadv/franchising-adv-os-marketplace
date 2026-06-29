---
name: competencia-foro-arbitragem-franquia
description: "Gestão processual chamada ANTES de toda peça de franquia: define o foro/juízo e trata a cláusula de arbitragem. Foro de eleição (CPC 63 + Lei 14.879/2024 — só vale com pertinência ao domicílio/residência de uma parte ou ao local da obrigação; juízo aleatório = abuso, declinável de ofício §3º/§5º) X cláusula compromissória de arbitragem (Lei 13.966 art. 7º §1º + Lei 9.307/96 art. 4º/8º Kompetenz-Kompetenz; preliminar CPC 337 X que o juiz NÃO conhece de ofício §5º, silêncio = renúncia §6º; tutela pré-arbitral CPC 305 + Lei 9.307 22-A/22-B). Use quando precisar definir onde ajuizar, qual o foro, há cláusula de arbitragem, competência, declinação, incompetência, preliminar de convenção de arbitragem, foro de eleição em contrato de franquia, tutela antes de instituir a arbitragem."
---

# COMPETENCIA-FORO-ARBITRAGEM-FRANQUIA

> Camada 1 (gestão processual transversal). Acionada **ANTES de toda inicial** e na defesa (preliminares de incompetência e de convenção de arbitragem). Em franquia a cláusula arbitral é comum — esta skill evita o foro errado **e** a perda da arbitragem.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§6 (competência/foro), §5.2 (preliminares 337 X), §4.4 (tutela pré-arbitral)**. `grep -niE "foro de eleic|arbitr|337|22-A" context/cpc-faixas-franquia.md`.
- `context/lei-13966-2019.md` — **art. 7º §1º** (autoriza arbitragem).
- `context/jurisprudencia-franquia.md` — **TEMA F** (foro de eleição + arbitragem ✅).

## Objetivo
Indicar com segurança o juízo competente (e o foro) **ou** reconhecer a competência arbitral, antecipando incompetência, declinação de ofício e a armadilha da renúncia à arbitragem.

## Quando ativar
- Antes de ajuizar (escolha do foro/juízo) — gate obrigatório.
- Na contestação, para arguir incompetência (CPC 337 II) **ou** convenção de arbitragem (CPC 337 X).
- Quando há cláusula compromissória e se precisa de tutela de urgência antes da arbitragem.

## Metodologia

1. **Premissa anti-CDC (não esquecer).** Franqueado **não é consumidor** (Lei 13.966 art. 1º) → **não** se aplica o foro do consumidor (CDC 101) nem a ressalva consumerista do CPC 63 §1º. Competência segue a **regra geral** (foro de eleição / domicílio do réu). Detalhe em `natureza-empresarial-nao-cdc`.

2. **FORO DE ELEIÇÃO — CPC 63 + Lei 14.879/2024 (verbatim):**
   > **Art. 63, §1º** *(redação da Lei nº 14.879/2024)*: a eleição de foro *"somente produz efeito quando constar de **instrumento escrito**, **aludir expressamente a determinado negócio jurídico** e **guardar pertinência com o domicílio ou a residência de uma das partes ou com o local da obrigação**, ressalvada a pactuação consumerista, quando favorável ao consumidor."*
   > **§3º** Antes da citação, a cláusula de eleição de foro, **se abusiva, pode ser reputada ineficaz de ofício** pelo juiz, que remeterá os autos ao foro de **domicílio do réu**.
   > **§4º** Citado, incumbe ao réu **alegar a abusividade na contestação, sob pena de preclusão**.
   > **§5º** *(Lei 14.879/2024)*: o **ajuizamento de ação em juízo aleatório** — sem vinculação com domicílio/residência das partes ou com o negócio — **constitui prática abusiva que justifica a declinação de competência de ofício**.

   **Aplicação em franquia:** a cláusula de eleição de foro (frequente no contrato) **só vale** com **pertinência** territorial (domicílio de uma parte OU local da obrigação). Foro escolhido sem âncora = **juízo aleatório** → declínio de ofício antes da citação (§3º/§5º); depois da citação, o réu argui na contestação sob pena de **preclusão** (§4º). Lei 14.879/2024 vigente desde **05.06.2024**.

3. **Foro supletivo (sem cláusula válida):** regra geral = **domicílio do réu** (CPC 46). Incompetência relativa argui-se como preliminar de contestação (CPC 64).

4. **CLÁUSULA DE ARBITRAGEM — quando existe, muda tudo.** Base: **Lei 13.966 art. 7º §1º** (*"As partes poderão eleger juízo arbitral para solução de controvérsias relacionadas ao contrato de franquia."*) + Lei 9.307/96:
   > **Art. 4º** A cláusula compromissória é a convenção pela qual as partes comprometem-se a submeter à arbitragem os litígios que possam vir a surgir; **§1º** deve ser estipulada **por escrito**.
   > **Art. 8º** A cláusula compromissória é **autônoma** em relação ao contrato... a nulidade deste não implica necessariamente a nulidade da cláusula. **Parágrafo único:** caberá **ao árbitro decidir** de ofício ou por provocação as questões sobre existência, validade e eficácia da convenção e do contrato. *(princípio **Kompetenz-Kompetenz**)*

   **Efeito:** havendo cláusula compromissória válida, **o Judiciário é incompetente** para o mérito; quem decide primeiro sobre a validade/alcance da cláusula é **o árbitro**.

5. **🔴 ARMADILHA — a preliminar de arbitragem (CPC 337 X):**
   > **Art. 337, X** — convenção de arbitragem (preliminar de contestação).
   > **§5º** *"Excetuadas a convenção de arbitragem e a incompetência relativa, o juiz conhecerá de ofício"* das matérias deste artigo → **a arbitragem o juiz NÃO conhece de ofício**.
   > **§6º** a **ausência de alegação** da convenção de arbitragem implica **aceitação da jurisdição estatal e renúncia ao juízo arbitral**.

   **Gravar:** havendo cláusula arbitral, **alegar a convenção de arbitragem como 1ª preliminar da contestação** (337 X). **Não alegar = renunciar** à arbitragem (§6º). Se o juiz **rejeitar** a preliminar, cabe **agravo de instrumento imediato** (CPC 1.015 III).

6. **TUTELA DE URGÊNCIA PRÉ-ARBITRAL (crítica para a liminar de bandeira).** Antes de instituído o tribunal arbitral, a urgência vai ao Judiciário:
   > **Lei 9.307/96 Art. 22-A** — *"Antes de instituída a arbitragem, as partes poderão recorrer ao Poder Judiciário para a concessão de medida cautelar ou de urgência."*
   > **Art. 22-B** — *"Instituída a arbitragem, caberá aos árbitros manter, modificar ou revogar a medida cautelar ou de urgência"* concedida pelo Judiciário.

   Veículo processual estatal: tutela cautelar antecedente **CPC 305** (fungível com a antecipada, 303). Depois de instituída a arbitragem, a competência **migra para os árbitros** (22-B). *(Lei 9.307 art. 22-A §único — prazo p/ requerer a instituição — 🟡 confirmar verbatim antes de citar.)*

7. **Jurisprudência ✅ (TEMA F):** STJ REsp 1.602.076/SP (Nancy Andrighi) — arbitragem é **válida** em franquia, mas, sendo **contrato de adesão**, a cláusula deve observar o **art. 4º §2º da Lei 9.307/96** (visto/destaque do aderente); cláusula "patológica" pode ser anulada *prima facie* pelo Judiciário. AgRg no REsp 1.336.491/SP (Buzzi) — foro de eleição em franquia é **válido** (sem relação consumerista).

## Entrega obrigatoria final
Decisão de gestão: (a) **há cláusula de arbitragem?** Se sim → competência arbitral + alerta da preliminar 337 X / renúncia 337 §6º + caminho da tutela pré-arbitral. (b) Se não → juízo/foro competente + fundamento (CPC 63/46) + alerta da Lei 14.879/2024 + (se defesa) minuta da preliminar de incompetência.

## Guard
Confirmar a redação vigente do art. 63 (Lei 14.879/2024) e dos arts. 337/22-A no anexo. Citação de julgado por `varredura-jurisprudencial-pre-tese` + `validador-franquia`. **Nenhuma peça sai sem passar por esta gestão.** Foro/arbitragem é item de R1 da `suprema-corte-franchising`.
