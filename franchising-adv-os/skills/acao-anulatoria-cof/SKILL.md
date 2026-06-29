---
name: acao-anulatoria-cof
description: "Redige a acao do FRANQUEADO que pede a anulabilidade/nulidade do contrato de franquia por Circular de Oferta de Franquia (COF) omissa, falsa ou entregue com menos de 10 dias de antecedencia (Lei 13.966/2019 art. 2º §1º/§2º + art. 4º), cumulada com a DEVOLUCAO corrigida da taxa de filiacao e dos royalties pagos. Pelo rito comum (CPC 319/327). Trata da decadencia (anulabilidade quadrienal CC 178) e do contraponto honesto (execucao prolongada convalida; mero insucesso nao anula — STJ REsp 1.881.149). Use quando o operador disser a COF era falsa/omissa, nao recebi a COF a tempo, recebi a circular junto com o contrato, quero anular o contrato de franquia, devolucao dos royalties, /acao-franquia anulatoria."
---

# ACAO-ANULATORIA-COF

> Camada 5 (Contencioso/conhecimento). Acao do FRANQUEADO que ataca o contrato por vicio da COF e pede devolucao corrigida. Gestao processual (competencia/arbitragem) obrigatoria ANTES.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2º** (23 incisos), **§1º** (entrega ≥ 10 dias antes), **§2º** (anulabilidade/nulidade + devolucao corrigida de filiacao e royalties), **art. 4º** (COF omissa/falsa). `grep -n "§ 1º\|§ 2º\|Art\. 4" context/lei-13966-2019.md`.
- `context/jurisprudencia-franquia.md` — **TEMA E** (COF deficiente → anulacao + devolucao; e o contraponto honesto). So ✅.
- `context/cpc-faixas-franquia.md` — CPC 319 (inicial), 327 (cumulacao), 292 (valor da causa). **grep + ler a faixa.**

## Objetivo
Anular o negocio (ou parte) e recuperar o que o franqueado pagou, com fundamento na letra da Lei 13.966 — sem prometer resultado que a jurisprudencia condiciona (prejuizo + tempo razoavel) e antecipando a defesa de convalidacao.

## Quando ativar
- COF nao entregue, entregue **junto** com o contrato/pagamento, entregue com **menos de 10 dias** (art. 2º §1º), **omissa** quanto a inciso obrigatorio ou com **informacao falsa** (art. 4º).
- O franqueado quer desfazer o contrato e ser restituido.

## Metodologia
1. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia` — **arbitragem PRIMEIRO** (clausula compromissoria? art. 7º §1º; mesmo a anulacao do contrato nao arrasta a clausula — autonomia, Lei 9.307 art. 8º; quem decide e o arbitro, Kompetenz-Kompetenz; salvo clausula "patologica") → **foro** com pertinencia (CPC 63, Lei 14.879/2024; sem ressalva consumerista — `natureza-empresarial-nao-cdc`). Carregar `base-legal-13966`.
2. **Mapear o vicio na COF (art. 2º, 23 incisos):** identificar exatamente qual inciso foi descumprido (ex.: III balancos, IV acoes judiciais, X desligados em 24 meses, XV know-how) **ou** o descumprimento do **prazo de 10 dias** (§1º). Distinguir:
   - **Anulabilidade** (vicio sanavel / descumprimento do §1º / omissao) — art. 2º §2º;
   - **Nulidade** (falsidade grave, objeto ilicito) — quando cabivel.
3. **`varredura-jurisprudencial-pre-tese` ANTES da tese** — entendimento atual do TJSP sobre o vicio invocado.
4. **Pedido (CPC 319/327):** (a) **anulabilidade ou nulidade** do contrato (conforme o caso); (b) **devolucao de TODAS as quantias pagas** ao franqueador ou a terceiros por ele indicados, a titulo de **filiacao ou royalties, corrigidas monetariamente** (art. 2º §2º — verbatim); (c) perdas e danos se comprovados. Art. 4º estende a sancao do §2º a quem "omitir informacoes exigidas por lei ou veicular informacoes falsas".
5. **Provar os requisitos da anulacao (TEMA E ✅):** o pedido exige **prejuizo comprovado** + **tempo razoavel** (TJSP Ap. 1018390-26.2022.8.26.0100 · 1ª CRDE · Rel. Des. Carlos Alberto de Salles ✅ — COF < 10 dias → anulacao + devolucao; pode haver **solidariedade da aceleradora/grupo economico**). Omissao de litigio/concorrencia desleal na COF → anulacao + restituicao (TJSP Ap. 1032315-87.2020.8.26.0576 · 1ª CRDE · Rel. Des. Cesar Ciampolini ✅), com contrapartida de devolver manual e descaracterizar pontos.
6. **Contraponto honesto (antecipar a defesa):** **execucao prolongada convalida**; alegar nulidade depois de executar = *venire contra factum proprium*; **mero insucesso e alea da franqueada**, nao da franqueadora — STJ REsp 1.881.149 · 3ª Turma · Rel. Min. Nancy Andrighi ✅. Avaliar tempo de operacao antes de ajuizar.
7. **Decadencia/prescricao:** **anulabilidade = decadencia quadrienal (CC 178)**; **nulidade absoluta (CC 166) nao convalesce nem decai (CC 169)**; cobranca/restituicao por inadimplemento = **decenal (CC 205)**. Fundamentos legais vigentes; o julgado de apoio especifico abre-se ao vivo via `validador-franquia`.

## Entrega obrigatoria final
- Inicial redigida (fatos + vicio da COF mapeado por inciso/prazo + pedido de anulabilidade/nulidade + devolucao corrigida + perdas e danos se houver + valor da causa) + checklist (COF recebida, data de entrega x assinatura, comprovantes de pagamento) + foro/vara ou clausula arbitral.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). Nao prometer anulacao sem **prejuizo + tempo razoavel**; sinalizar o risco de convalidacao. CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente — acordao antigo mapeado para a 13.966. Calculo da devolucao corrigida → cross-link `calculosjudiciais-adv-os`. Fecha pela `suprema-corte-franchising` (R1-R4).
