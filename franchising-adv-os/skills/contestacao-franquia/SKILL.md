---
name: contestacao-franquia
description: "Redige a contestacao SIDE-AWARE em litigio de franquia (defende o FRANQUEADO ou a FRANQUEADORA), em peca unica, no prazo de 15 dias (CPC 335). Concentra toda a defesa (CPC 336): preliminares do art. 337 — com destaque para a CONVENCAO DE ARBITRAGEM (inciso X), que o juiz NAO conhece de oficio (§5º) e cujo silencio = renuncia (§6º), e para a incompetencia/foro abusivo (Lei 14.879/2024, CPC 64) e a incorrecao do valor da causa (III) — mais a impugnacao especificada dos fatos (CPC 341) e o merito por lado (franqueado: COF viciada, falha de suporte/exclusividade; franqueadora: inadimplemento, COF valida, convalidacao). Use quando o operador disser fui citado na franquia, contestar, defesa do franqueado/franqueadora, prazo de contestacao, vou responder a acao de franquia."
---

# CONTESTACAO-FRANQUIA

> Camada 5 (Contencioso/conhecimento). Defesa concentrada do reu, **side-aware** (franqueado OU franqueadora). Definir o LADO antes de redigir. Gestao processual (competencia/arbitragem) obrigatoria.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§5/§6** (defesa): CPC 335 (prazo 15d), 336 (concentracao), **337 (preliminares, esp. X arbitragem, §5º/§6º)**, 341 (impugnacao especificada), 343 (reconvencao), 63/64 (foro/incompetencia). **grep + ler a faixa.**
- `context/lei-13966-2019.md` — art. 2º (COF/incisos), §1º/§2º, art. 4º (vicio da COF — defesa do franqueado); art. 7º §1º (arbitragem). `grep -n`.
- `context/jurisprudencia-franquia.md` — TEMA A (sem CDC), TEMA E (convalidacao — defesa da franqueadora), TEMA B/C (limites). So ✅.

## Objetivo
Apresentar defesa tecnicamente fechada, sem deixar fato sem impugnacao e **sem perder a arbitragem por silencio**, com o merito ajustado ao lado defendido.

## Quando ativar
- O cliente (franqueado ou franqueadora) foi citado e ha prazo de defesa.
- Necessidade de avaliar preliminares (arbitragem, foro, valor) e o merito por lado.

## Metodologia
1. **Definir o LADO** (franqueado x franqueadora) — comanda todo o merito.
2. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia` + `base-legal-13966` + `natureza-empresarial-nao-cdc` (afastar CDC se o autor invocar foro do consumidor/inversao do onus).
3. **Tempestividade:** prazo de **15 dias** (CPC 335) — termo inicial conforme os incisos (audiencia 334, protocolo de desistencia, juntada do AR/citacao).
4. **Concentracao (CPC 336):** "incumbe ao reu alegar... **toda a materia de defesa**" e especificar as provas. O que nao for alegado preclui.
5. **Preliminares (CPC 337) — ANTES do merito:**
   - **X — convencao de arbitragem (ARMADILHA, gravar):** e a **unica** preliminar que o juiz **nao conhece de oficio** (§5º) e cujo **silencio = aceitacao da jurisdicao estatal e renuncia ao juizo arbitral** (§6º). Em franquia a clausula arbitral e comum (art. 7º §1º) → **alegar no 1º momento sob pena de renuncia**. Rejeitada → cabe AI imediato (CPC 1.015 III).
   - **II/incompetencia + foro abusivo:** CPC 64; cláusula de eleicao sem **pertinencia** (Lei 14.879/2024 — CPC 63) e abusiva → alegar na contestacao sob pena de preclusao (63 §4º). **Sem ressalva consumerista** (franqueado nao e consumidor).
   - **III — incorrecao do valor da causa** (CPC 293), se cumulacao mal somada (CPC 292 VI).
   - Demais cabiveis (inepcia IV, ilegitimidade XI etc.).
6. **Impugnacao especificada (CPC 341):** manifestar-se **precisamente sobre cada fato** da inicial — "presumem-se verdadeiras as nao impugnadas". Nao deixar fato sem resposta.
7. **`varredura-jurisprudencial-pre-tese` ANTES de fechar as teses de merito** (convalidacao, limites da nao-concorrencia, COF viciada) — confirmar o entendimento atual TJSP/STJ.
8. **Merito por LADO:**
   - **Defendendo o FRANQUEADO:** COF viciada/omissa/falsa ou fora do prazo de 10 dias (art. 2º §1º/§2º + art. 4º); descumprimento de suporte/treinamento/exclusividade territorial pela franqueadora; nao-concorrencia/bandeira ampla demais (limites — TEMA B/C ✅); multa excessiva → reducao por equidade (CC 413, ordem publica — STJ REsp 1.898.738 ✅); pedir reconvencao se houver devolucao a cobrar (`reconvencao-franquia`).
   - **Defendendo a FRANQUEADORA:** inadimplemento do franqueado (royalties/fundo/taxas); COF entregue e completa; **convalidacao** por execucao prolongada / *venire contra factum proprium* / insucesso = alea (STJ REsp 1.881.149 ✅); multa devida; pedir reconvencao por debitos+multa.
9. **Provas:** especificar e requerer (documental ja instruida; **pericia contabil** para royalties sobre faturamento; testemunhal com rol).
10. **Reconvencao (CPC 343):** se ha pretensao propria conexa, na mesma peca via `reconvencao-franquia`.

## Entrega obrigatoria final
- Contestacao redigida (preliminares ordenadas — arbitragem em destaque + impugnacao especificada item a item + merito por lado + provas) + reconvencao se cabivel + rol de testemunhas + prazo confirmado.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). **NUNCA esquecer a preliminar de arbitragem** (337 X — silencio = renuncia, §6º). Nao deixar fato sem impugnacao (341). CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente. Fecha pela `suprema-corte-franchising` (R1-R4).
