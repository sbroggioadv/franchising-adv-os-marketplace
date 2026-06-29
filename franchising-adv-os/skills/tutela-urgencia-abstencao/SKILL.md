---
name: tutela-urgencia-abstencao
description: "Redige o pedido de tutela de urgencia de abstencao para cessar IMEDIATAMENTE o uso da marca/identidade/sistema pelo ex-franqueado ('virar a bandeira'). Monta os requisitos do CPC 300 (probabilidade do direito + perigo de dano; §3º veda a antecipada irreversivel; §1º caucao), as astreintes do CPC 537 (multa diaria, ajustavel de oficio, devida ao exequente) e os meios de efetivacao do CPC 536 §1º (busca e apreensao, remocao de material de marca, forca policial), alem da LPI art. 209 §1º (liminar antes da citacao). Decide entre antecedente (CPC 303/304 estabilizacao ou cautelar 305/308) e incidental, e a via PRE-ARBITRAL (Lei 9.307 art. 22-A/22-B). Use quando o operador disser quero a liminar de abstencao, preciso parar o uso da marca agora, liminar para virar a bandeira, multa diaria, tutela de urgencia na franquia."
---

# TUTELA-URGENCIA-ABSTENCAO

> Camada 5 (Contencioso/conhecimento). A liminar de abstencao que sustenta a acao de bandeira/rescisao. Acoplada a `concorrencia-desleal-bandeira` e a `acao-rescisao-franquia`. Gestao processual (competencia/arbitragem) obrigatoria ANTES.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§4** (tutela de abstencao): CPC 300 (§1º/§2º/§3º), 301 (meios cautelares), 537 (§1º/§2º/§4º astreintes), 536 §1º (efetivacao), 294 §ú, 303/304 (antecipada antecedente + estabilizacao), 305/308/309 (cautelar antecedente), Lei 9.307 22-A/22-B (pre-arbitral). **grep + ler a faixa.**
- `context/lpi-concorrencia-desleal.md` — **art. 209 §1º** (sustacao liminar antes da citacao) + §2º (apreensao). `grep -n "209"`.
- `context/jurisprudencia-franquia.md` — **TEMA C** (abstencao de marca/limites). So ✅.

## Objetivo
Obter a ordem de cessacao imediata do uso indevido, com multa diaria eficaz e meios de cumprimento, escolhendo a via processual correta (incidental, antecedente ou pre-arbitral) e respeitando o limite de irreversibilidade.

## Quando ativar
- Urgencia em fazer cessar o uso de marca/sistema (em geral pela `concorrencia-desleal-bandeira` ou `acao-rescisao-franquia`).
- Pode ser side-aware: tambem para **resistir/derrubar** liminar concedida (apontar ausencia de probabilidade/perigo, ou irreversibilidade — CPC 300 §3º).

## Metodologia
1. **Gestao processual SEMPRE (C1) ANTES:** `competencia-foro-arbitragem-franquia`. **Atencao a arbitragem:** se ha clausula compromissoria (art. 7º §1º), a urgencia **antes** de instituida a arbitragem vai ao **Judiciario** — Lei 9.307 **art. 22-A**; **instituida**, a competencia migra para os arbitros (manter/modificar/revogar) — **art. 22-B**. So o Judiciario nessa janela inicial.
2. **`varredura-jurisprudencial-pre-tese` ANTES da tese** (probabilidade) — entendimento atual sobre abstencao de marca x atividade.
3. **Requisitos (CPC 300):** "havera tutela de urgencia quando houver elementos que evidenciem a **probabilidade do direito e o perigo de dano** ou o risco ao resultado util do processo". **Probabilidade** = contrato + clausula de nao-uso pos-contratual + COF (Lei 13.966 art. 2º XV) + prova do uso atual. **Perigo** = diluicao/confusao de marca e dano a rede a cada dia. §2º pode ser concedida liminarmente ou apos justificacao previa; **§3º a antecipada NAO se concede quando houver perigo de irreversibilidade**; §1º o juiz pode exigir **caucao** (dispensavel ao hipossuficiente).
4. **Base material reforcada:** **LPI art. 209 §1º** — o juiz pode "determinar liminarmente a sustacao da violacao... **antes da citacao do reu**", mediante caucao se necessario. Somar a CPC 300.
5. **Astreintes (CPC 537):** multa independe de requerimento, aplicavel em tutela provisoria, **suficiente e compativel** com a obrigacao, com **prazo razoavel**; §1º o juiz pode **modificar valor/periodicidade** de oficio; §2º **devida ao exequente**; §4º devida desde o descumprimento. Dimensionar para coagir sem confiscar.
6. **Meios de efetivacao (CPC 536 §1º):** "imposicao de multa, a busca e apreensao, a remocao de pessoas e coisas, o desfazimento de obras e o impedimento de atividade nociva... auxilio de forca policial" — pedir remocao/busca e apreensao de material de marca; CPC 301 (arresto/sequestro) e LPI 209 §2º (apreensao em reproducao flagrante de marca registrada).
7. **Escolher a via (CPC 294 §ú — antecedente x incidental):**
   - **Incidental:** dentro da acao principal (bandeira/rescisao) — o caminho usual.
   - **Antecipada ANTECEDENTE (CPC 303):** urgencia contemporanea a propositura; inicial limitada ao requerimento + indicacao do pedido final; aditar em **15 dias** (§1º I; §2º nao aditou → extincao); indicar o §5º; pode **estabilizar** (CPC 304) se nao houver recurso.
   - **Cautelar ANTECEDENTE (CPC 305):** inicial sumaria; efetivada, o **pedido principal em 30 dias** (CPC 308); cessa a eficacia se nao deduzido (CPC 309). Fungibilidade com a antecipada (305 §ú).
8. **Limite (nao errar):** a abstencao recai sobre **marca/trade dress/sistema**, **nao** sobre a atividade do ex-franqueado (TEMA C ✅) — pedido amplo demais e indeferido.

## Entrega obrigatoria final
- Peticao/capitulo de tutela redigido (probabilidade + perigo demonstrados + pedido de abstencao com limites + astreintes dimensionadas + meios de efetivacao + via escolhida e justificada + observacao pre-arbitral se houver clausula) + indicacao de caucao se exigida.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia` (so ✅, nº+orgao). Checar **irreversibilidade** (CPC 300 §3º) e **arbitragem** (22-A/22-B) antes de protocolar no Judiciario. Abstencao **com limites**. CDC nao incide entre as partes (art. 1º); nunca a 8.955/94 como vigente. Recurso contra (in)deferimento da liminar → `agravo-de-instrumento-franquia` (CPC 1.015 I). Fecha pela `suprema-corte-franchising` (R1-R4).
