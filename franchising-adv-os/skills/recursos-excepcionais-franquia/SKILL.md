---
name: recursos-excepcionais-franquia
description: "Redige Recurso Especial (CPC 1.029 §1o — dissidio jurisprudencial; prequestionamento via 1.025 + ED) e Recurso Extraordinario (CPC 1.035 — repercussao geral) em franquia, com as DUAS BARREIRAS centrais do dominio gravadas: Sumula 5/STJ (a simples interpretacao de clausula contratual NAO enseja REsp) e Sumula 7/STJ (o simples reexame de prova NAO enseja REsp). Grande parte das teses de franquia (alcance da nao-concorrencia, base de royalties, clausula penal) e interpretacao de clausula e NAO sobe; litigio e infraconstitucional (RE estreito). Orienta a tangenciar as sumulas formulando questao de DIREITO FEDERAL, nao releitura de clausula. Use quando o operador disser REsp, recurso especial, recurso extraordinario, RE, levar ao STJ/STF, dissidio jurisprudencial, repercussao geral, prequestionamento."
---

# RECURSOS-EXCEPCIONAIS-FRANQUIA

> Camada 7 (recursos). Acesso as cortes superiores (STJ/STF). Em franquia, a maior dificuldade NAO e redigir — e **passar pelas Sumulas 5 e 7/STJ**. Side-aware: recorre a parte vencida no acordao.

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§7.4 (REsp 1.029 §1o + Sumulas 5 e 7/STJ ✅)**, **§7.5 (RE 1.035 repercussao geral)**, **§7.3 (ED 1.022/1.025 prequestionamento)**. `grep -niE "1.029|1.035|1.025|Sumula 5|Sumula 7|prequest" context/cpc-faixas-franquia.md`.
- `context/jurisprudencia-franquia.md` — tese de fundo + julgado-ancora (so ✅; dissidio exige paradigma real).
- `context/lei-13966-2019.md` — a **materia federal** prequestionada (qual dispositivo da 13.966 foi violado?).

## Objetivo
Viabilizar o REsp/RE quando ha materia federal/constitucional, **superando as Sumulas 5 e 7/STJ** com o enquadramento correto — e nao deixar subir o que e mera interpretacao de clausula ou reexame de prova (perda de tempo e de honorarios).

## Quando ativar
- Acordao do tribunal de 2o grau em causa de franquia, e a parte quer levar ao STJ (REsp) ou STF (RE).
- Gatilhos: "REsp", "recurso especial", "recurso extraordinario", "STJ", "STF", "dissidio", "repercussao geral", "prequestionamento".

## Metodologia

### 1. Prequestionamento — pre-requisito (CPC 1.025 + ED 1.022)
> **Art. 1.025** — consideram-se incluidos no acordao os elementos que o embargante suscitou **para fins de prequestionamento**, ainda que os ED sejam inadmitidos/rejeitados, caso o tribunal superior considere existentes erro/omissao/contradicao/obscuridade. *(prequestionamento ficto)*

Sem a materia federal **debatida no acordao**, o REsp nao sobe. Opor **ED (1.022)** para prequestionar antes (cross-link `apelacao-franquia`).

### 2. REsp — CPC 1.029 §1o (verbatim) e as DUAS BARREIRAS
> **Art. 1.029** — REsp e RE interpostos perante o presidente/vice do tribunal recorrido, em peticoes distintas: I exposicao do fato e do direito; II demonstracao do cabimento; III razoes da reforma. **§1o** — fundado em **dissidio jurisprudencial**, provar a divergencia (certidao/copia/repositorio oficial ou julgado na internet), **mencionando as circunstancias que assemelhem os casos**.

> 🔴 **AS DUAS BARREIRAS CENTRAIS DE FRANQUIA (gravar):**
> - **Sumula 5/STJ ✅** — *"A simples interpretacao de clausula contratual nao enseja recurso especial."* Barreira central: alcance da nao-concorrencia, base de calculo de royalties, redacao da clausula penal, exclusividade territorial — **tudo isso e interpretacao de clausula** e **nao sobe** por essa via.
> - **Sumula 7/STJ ✅** — *"A pretensao de simples reexame de prova nao enseja recurso especial."* Bloqueia rediscutir fatos/provas (ex.: se houve ou nao prejuizo na COF, se a marca foi usada).

### 3. Como TANGENCIAR as Sumulas 5 e 7 (a engenharia da tese)
- **Nao** pedir "releitura da clausula" -> formular **questao de DIREITO FEDERAL**: *qual norma da Lei 13.966/2019 / CC / CPC / Lei 9.307/96 o acordao violou na qualificacao juridica do fato* (ex.: o acordao **negou vigencia** ao art. 2o §2o da 13.966 ao manter contrato com COF entregue fora dos 10 dias — questao de direito, nao de clausula).
- **Nao** pedir reexame de prova -> partir da **moldura factica fixada pelo acordao** e discutir a **consequencia juridica** (valoracao juridica do fato incontroverso ≠ reexame).
- **Dissidio (§1o):** escolher **paradigma real e analogo** (julgado ✅ de outra corte com a mesma base factica) — confrontar circunstancias. Paradigma inventado/inadequado = inadmissao.

### 4. RE — CPC 1.035 (repercussao geral)
> **Art. 1.035** — o STF nao conhecera do RE quando a questao constitucional **nao tiver repercussao geral**; **§1o** questoes relevantes (economico/politico/social/juridico) que ultrapassem os interesses subjetivos; **§2o** o recorrente **deve demonstrar** a repercussao geral (preliminar formal e fundamentada).

Litigio de franquia e, em regra, **infraconstitucional** (13.966/CC/CPC/9.307) -> o **RE e via estreita**; o caminho ordinario e o **REsp** (ainda assim filtrado pelas Sumulas 5 e 7). So insistir no RE havendo **questao constitucional direta** (ex.: livre iniciativa/profissao na nao-concorrencia — confirmar tese ao vivo).

## Entrega obrigatoria final
- REsp e/ou RE em peticoes distintas (1.029) com: prequestionamento demonstrado (ED/1.025), enquadramento que **supera as Sumulas 5 e 7** (questao de direito federal, nao de clausula/prova), dissidio com paradigma real (§1o) quando for o caso, e — no RE — preliminar de repercussao geral (1.035 §2o). Parecer franco sobre a **chance de admissao** (filtro das sumulas).

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia`. **Paradigma de dissidio e julgado de fundo so ✅ verificados ao vivo** (`varredura-jurisprudencial-pre-tese` + guard global). Sumulas 5 e 7/STJ ✅ conferidas no anexo. Nao deixar subir tese que e pura interpretacao de clausula/reexame (avisar o operador). Entrega fecha pela `suprema-corte-franchising`.
