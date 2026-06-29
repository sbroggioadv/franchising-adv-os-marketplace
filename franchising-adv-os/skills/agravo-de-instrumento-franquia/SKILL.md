---
name: agravo-de-instrumento-franquia
description: "Redige agravo de instrumento (CPC 1.015) contra decisao interlocutoria no contencioso de franquia, com foco nos incisos criticos do dominio: I (tutela provisoria — recorre da liminar de bandeira/abstencao CONCEDIDA ou NEGADA), III (rejeicao da alegacao de convencao de arbitragem — quando o juiz mantem a causa no Judiciario apesar da clausula compromissoria) e X (concessao/modificacao/revogacao do efeito suspensivo aos embargos a execucao). Forma 1.016/1.017 (peticao direta ao tribunal + pecas obrigatorias), prazo 15 dias uteis. Use quando o operador disser agravar, agravo de instrumento, recorrer da liminar, recorrer da decisao que negou/concedeu a tutela de bandeira, o juiz rejeitou a arbitragem, decisao interlocutoria na execucao."
---

# AGRAVO-DE-INSTRUMENTO-FRANQUIA

> Camada 7 (recursos). Recurso contra **decisao interlocutoria** (nao sentenca). Critico em franquia para a **liminar de bandeira** (tutela de abstencao) e para a **rejeicao da arbitragem**. Side-aware: agrava quem foi prejudicado pela interlocutoria (franqueador ou franqueado).

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§7.1 (1.015 incisos I/III/X + forma 1.016/1.017)**, **§4 (tutela de urgencia 300 — para combater/sustentar a liminar)**, **§6.2 (arbitragem)**. `grep -niE "1.015|1.016|1.017|agravo|arbitr" context/cpc-faixas-franquia.md`.
- `context/lei-13966-2019.md` — **art. 7o §1o** (arbitragem) quando o agravo for do inciso III.
- `context/lpi-concorrencia-desleal.md` — **art. 209 §1o** (liminar de abstencao) quando o agravo for do inciso I (bandeira).
- `context/jurisprudencia-franquia.md` — **Tema C/F** (so apos confirmar).

## Objetivo
Levar ao tribunal a interlocutoria recorrivel (1.015), com a peca formalmente perfeita (1.016/1.017) e pedido de **efeito suspensivo** ou **tutela antecipada recursal**, atacando ou sustentando a liminar de bandeira / a decisao sobre arbitragem.

## Quando ativar
- Foi proferida **decisao interlocutoria** recorrivel por AI: liminar de abstencao concedida ou negada; rejeicao da preliminar de arbitragem; decisao sobre efeito suspensivo dos embargos.
- Gatilhos: "agravar", "recorrer da liminar", "negaram a tutela de bandeira", "concederam a liminar contra meu cliente", "o juiz rejeitou a arbitragem", "decisao na execucao".

## Metodologia

### 1. Cabimento — CPC 1.015 (rol; incisos do dominio, verbatim)
> **Art. 1.015** — cabe AI contra interlocutorias que versarem sobre: **I - tutelas provisorias**; II - merito; **III - rejeicao da alegacao de convencao de arbitragem**; ... **X - concessao, modificacao ou revogacao do efeito suspensivo aos embargos a execucao** ... **Paragrafo unico** — cabe AI tambem contra interlocutorias na **liquidacao/cumprimento de sentenca, no processo de execucao e no inventario**.

> **Tres frentes de franquia:**
> - **I (tutela provisoria)** -> recorre-se da decisao que **concede ou nega a liminar de abstencao** ("virar a bandeira"). E o uso mais comum do AI no dominio. Sustentar/atacar com CPC 300 (probabilidade + perigo) + LPI 209 §1o.
> - **III (rejeicao da convencao de arbitragem)** -> se o juiz **rejeita** a preliminar de arbitragem (337 X) e segue no Judiciario, cabe **AI imediato** (a clausula compromissoria e comum em franquia — art. 7o §1o).
> - **X (efeito suspensivo dos embargos)** + paragrafo unico (execucao) -> interlocutorias da execucao do contrato de franquia.

### 2. Tempestividade
**15 dias uteis** (prazo recursal — CPC 1.003 §5 c/c 219; confirmar a contagem ao vivo se necessario — o anexo traz a forma, nao o prazo). Dobro para os sujeitos com prazo em dobro.

### 3. Forma — CPC 1.016 / 1.017 (verbatim)
> **Art. 1.016** — o AI sera dirigido **diretamente ao tribunal**, com: I nomes/qualificacao; II exposicao do fato e do direito; III razoes do pedido de reforma/invalidacao e o proprio pedido; IV nome/endereco dos advogados.
> **Art. 1.017, I** — a peticao sera instruida **obrigatoriamente** com copias da decisao agravada, da certidao da intimacao (ou prova da data de ciencia) e das procuracoes.

Montar o **instrumento** (peca + pecas obrigatorias). Falta de peca obrigatoria = inadmissao — checklist rigoroso.

### 4. Efeito suspensivo / tutela recursal
Pedir ao relator a **suspensao da eficacia** da decisao ou a **antecipacao da tutela recursal**, demonstrando probabilidade de provimento + risco de dano grave. Na bandeira: se a liminar foi **negada**, pedir a tutela recursal para cessar o uso ja (LPI 209 §1o + CPC 300 + astreintes 537); se foi **concedida** contra o cliente, pedir efeito suspensivo (atacar probabilidade/perigo e a **irreversibilidade**, 300 §3o).

### 5. Conteudo do merito recursal por frente
- **Bandeira (I):** rediscutir probabilidade do direito (contrato + clausula de bandeira + COF art. 2o XV-b) e perigo (diluicao/confusao de marca); ou, do lado do ex-franqueado, os **limites** da clausula (nao aniquilar a atividade — Tema B/C 🟡).
- **Arbitragem (III):** Kompetenz-Kompetenz (Lei 9.307 art. 8o §u — quem decide e o arbitro); clausula valida em adesao se observado o art. 4o §2o (Tema F 🟡).
- **Execucao (X / §u):** efeito suspensivo dos embargos / atos de constricao.

## Entrega obrigatoria final
- AI dirigido ao tribunal (1.016) + razoes atacando a interlocutoria por frente (I/III/X) + pedido de efeito suspensivo/tutela recursal + **checklist das pecas obrigatorias (1.017 I)** + parecer de tempestividade.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. Prazo recursal (15 dias uteis) — a forma 1.016/1.017 e ✅ no anexo; **confirmar a contagem do prazo ao vivo**. Jurisprudencia (Temas B/C/F) so apos `varredura-jurisprudencial-pre-tese`. Gestao (arbitragem) por `competencia-foro-arbitragem-franquia`. Entrega fecha pela `suprema-corte-franchising`.
