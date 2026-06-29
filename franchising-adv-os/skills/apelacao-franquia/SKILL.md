---
name: apelacao-franquia
description: "Redige apelacao (CPC 1.009-1.014) contra sentenca no contencioso de franquia, com atencao as EXCECOES de efeito suspensivo do dominio: a regra e o efeito suspensivo (1.012), MAS comecam a produzir efeitos imediatos (sem suspensivo) a sentenca que julga IMPROCEDENTES os embargos do executado (§1o III — franqueador executa royalties e prossegue o cumprimento), que institui ARBITRAGEM (§1o IV) e que confirma/concede/revoga TUTELA PROVISORIA (§1o V — liminar de bandeira). Teoria da causa madura (1.013 §3o) e preliminar de apelacao para interlocutorias nao-agravaveis (1.009 §1o). Use quando o operador disser apelar, apelacao, recorrer da sentenca, sentenca de franquia improcedente, efeito suspensivo da apelacao, causa madura."
---

# APELACAO-FRANQUIA

> Camada 7 (recursos). Recurso por excelencia contra a **sentenca** de franquia (rescisao, anulatoria de COF, concorrencia desleal, embargos). Side-aware: apela a parte sucumbente.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§7.2 (apelacao 1.009-1.014, esp. 1.012 §1o III/IV/V e 1.013 §3o causa madura)**, **§7.3 (ED 1.022 — prequestionar antes de subir)**. `grep -niE "1.009|1.012|1.013|apelac|efeito suspensiv" context/cpc-faixas-franquia.md`.
- `context/lei-13966-2019.md` — fundamentacao de merito (a sentenca aplicou a **13.966/2019 vigente**, nunca a 8.955/94?).
- `context/jurisprudencia-franquia.md` — temas pertinentes ao merito (so apos confirmar).

## Objetivo
Reformar ou anular a sentenca com razoes que ataquem cada capitulo, tempestiva, com o **pedido de efeito correto** (e ciencia de quando a sentenca de franquia ja produz efeitos imediatos) e, quando cabivel, requerendo a causa madura.

## Quando ativar
- Houve **sentenca** (485 terminativa ou 487 definitiva) em causa de franquia e a parte quer recorrer.
- Gatilhos: "apelar", "apelacao", "recorrer da sentenca", "julgaram improcedente", "efeito suspensivo", "causa madura".

## Metodologia

### 1. Cabimento e tempestividade
> **Art. 1.009** — da **sentenca** cabe apelacao. **§1o** — questoes resolvidas na fase de conhecimento **nao cobertas pela preclusao** (que nao comportavam AI) sao suscitadas em **preliminar de apelacao ou nas contrarrazoes**.

Levantar as interlocutorias **nao-agravaveis** em preliminar (§1o). Prazo **15 dias uteis** (confirmar contagem ao vivo). Forma 1.010: peticao ao **juizo de 1o grau** + razoes; apelado intimado para contrarrazoes (15 dias); remessa **independe de juizo de admissibilidade na origem** (§3o).

### 2. Efeitos — CPC 1.012 (verbatim; o ponto sensivel da franquia)
> **Art. 1.012** — a apelacao tera **efeito suspensivo**. **§1o** — **comeca a produzir efeitos imediatamente** (sem suspensivo) a sentenca que: ... **III - extingue sem resolucao do merito ou julga IMPROCEDENTES OS EMBARGOS DO EXECUTADO**; **IV - julga procedente o pedido de INSTITUICAO DE ARBITRAGEM**; **V - confirma, concede ou revoga TUTELA PROVISORIA** ... **§4o** — o relator pode suspender a eficacia se houver probabilidade de provimento ou risco de dano grave.

> **As tres excecoes que mais aparecem em franquia:**
> - **§1o III** — sentenca que julga **improcedentes os embargos do executado** (defesa do franqueado na execucao de royalties/fundo/multa) **NAO tem efeito suspensivo** na apelacao -> o franqueador **prossegue** com o cumprimento provisorio. Do lado do franqueado, pedir efeito suspensivo *ope iudicis* ao relator (§4o).
> - **§1o IV** — sentenca que **institui arbitragem** produz efeito imediato.
> - **§1o V** — sentenca que confirma/concede/revoga **tutela provisoria** (liminar de bandeira) produz efeito imediato.

### 3. Error in procedendo x in judicando
Estruturar **preliminares de nulidade** (in procedendo) e o **merito recursal** (in judicando), atacando cada fundamento. Conferir que a sentenca fundou-se na **Lei 13.966/2019** (nunca 8.955/94) e tratou o **CDC nos dois eixos** corretos (franqueador x franqueado SEM CDC; rede x consumidor COM).

### 4. Causa madura — CPC 1.013 §3o (verbatim)
> **Art. 1.013** — a apelacao **devolve ao tribunal o conhecimento da materia impugnada**. **§3o** — se o processo estiver em **condicoes de imediato julgamento**, o tribunal **decide desde logo o merito** (reformar sentenca 485, decretar nulidade, suprir omissao de pedido).

Requerer **expressamente** a causa madura quando favoravel (evita devolucao dos autos a origem).

### 5. Questoes de fato novas
> **Art. 1.014** — questoes de fato **nao propostas** no juizo inferior so na apelacao se a parte **provar forca maior**.

## Entrega obrigatoria final
- Peticao de interposicao + razoes combatendo cada fundamento (preliminares in procedendo + merito in judicando) + **pedido de efeito correto** (atencao as excecoes do 1.012 §1o III/IV/V; pedido de efeito suspensivo ope iudicis quando preciso) + requerimento de causa madura quando favoravel + parecer de tempestividade.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. Confirmar a contagem do prazo (15 dias uteis) ao vivo. Jurisprudencia so apos `varredura-jurisprudencial-pre-tese`. Prequestionar (ED 1.022) o que devera subir em REsp/RE -> `recursos-excepcionais-franquia`. Entrega fecha pela `suprema-corte-franchising`.
