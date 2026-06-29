---
name: transferencia-cessao-renovacao
description: "Trata a TRANSFERENCIA/CESSAO da franquia e a SUCESSAO (Lei 13.966 art. 2o XVII — a COF deve declarar se ha regras e quais) e a RENOVACAO do contrato (art. 2o XXII — especificacao precisa do prazo e das condicoes de renovacao): requisitos, ANUENCIA do franqueador, due diligence do cessionario, e os instrumentos (instrumento de cessao com anuencia; aditivo/novo contrato de renovacao). Cobre transferencia inter vivos, cessao a terceiro, sucessao por falecimento e renovacao/prorrogacao no fim do prazo. Use quando o operador disser transferir a franquia, vender minha unidade, ceder o contrato de franquia, passar a franquia para outro, sucessao na franquia, herdeiro assumir a unidade, renovar o contrato de franquia, prorrogar a franquia, fim do prazo da franquia."
---

# TRANSFERENCIA-CESSAO-RENOVACAO

> Consultivo/contratual (diferencial). Movimenta a **titularidade** (transferencia/cessao/sucessao) ou prolonga a **vigencia** (renovacao) da franquia. Lado: em regra **franqueado** (que transfere/renova), com a **anuencia do franqueador** como eixo. Side-aware quando o franqueador quer regrar/recusar.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2o XVII (transferencia/sucessao), XXII (prazo/renovacao), XVI (contrato-padrao)**, **art. 3o (sublocacao: legitimidade para renovar a locacao/sublocacao)**. `grep -niE "XVII|XXII|XVI|art. 3" context/lei-13966-2019.md`.
- `context/manuais-estrutura.md` — perfil do franqueado e padrao a ser mantido (o cessionario tera de seguir o DNA).
- `context/financeiro-dre.md` — taxa de renovacao (~1a vigencia + correcao 🟡) e taxa de transferencia, se previstas na COF/contrato.
- `context/jurisprudencia-franquia.md` — temas pertinentes (so apos confirmar).

## Objetivo
Formalizar a operacao certa (transferencia, cessao, sucessao ou renovacao) com os requisitos da COF/contrato, a anuencia do franqueador e o instrumento adequado — preservando o padrao da rede e a coerencia COF/contrato.

## Quando ativar
- O franqueado quer **vender/transferir/ceder** a unidade, ou ha **sucessao** (falecimento/herdeiros), ou o contrato esta no **fim do prazo** e ha **renovacao/prorrogacao** a tratar.
- Gatilhos: "transferir a franquia", "vender minha unidade", "ceder o contrato", "sucessao", "herdeiro assumir", "renovar o contrato", "prorrogar a franquia", "fim do prazo".

## Metodologia

### 1. Identificar a operacao + verificar a base na COF/contrato
- A COF declara **se ha** regras de transferencia/sucessao e **quais** (art. 2o XVII)? E o **prazo e as condicoes de renovacao** (art. 2o XXII)? O ponto de partida e sempre o que o contrato-padrao (XVI) e a COF fixaram — a lei nao impoe um regime unico; remete ao que foi pactuado/declarado.

### 2. Transferencia / cessao (inter vivos)
- **Anuencia do franqueador** e o eixo: o contrato de franquia e *intuitu personae* (perfil do franqueado — art. 2o VI); a cessao sem anuencia, quando o contrato a exige, e ineficaz/quebra contratual.
- **Due diligence do cessionario:** o novo franqueado atende o perfil (VI) e os requisitos de envolvimento (VII)? O franqueador costuma exigir treinamento e aprovacao.
- **Saneamento de pendencias:** quitar royalties/fundo/multas em aberto antes de transferir (senao o passivo segue/contamina).
- **Instrumento:** **instrumento de cessao de contrato de franquia** com (a) anuencia expressa do franqueador, (b) sub-rogacao do cessionario nos direitos/deveres, (c) responsabilidade por passivos anteriores, (d) eventual **taxa de transferencia** se prevista. Se ha **sublocacao** do ponto (art. 3o), tratar a locacao em conjunto (legitimidade para renovar — art. 3o).

### 3. Sucessao (falecimento do franqueado)
- Verificar se a COF/contrato (XVII) preve a **sucessao por herdeiros** e em que condicoes (alguns contratos permitem, outros preveem extincao/recompra).
- Habilitar o(s) herdeiro(s)/espolio conforme o pactuado; manter o padrao e o perfil; formalizar a sucessao por aditivo com anuencia do franqueador. Sem regra previa, negociar caso a caso.

### 4. Renovacao / prorrogacao (art. 2o XXII)
- Conferir o **prazo** vigente e as **condicoes de renovacao** declaradas (XXII): antecedencia para manifestar interesse, requisitos (adimplencia, padrao, reforma/reinvestimento para padrao atual), **taxa de renovacao** (financeiro-dre §4.1 — referencia 🟡, conforme contrato).
- **Instrumento:** **aditivo de renovacao** ou **novo contrato** (atualizando COF/condicoes a versao atual da rede). Atencao a **revisao de royalties/fundo** na renovacao — coerencia com a base do contrato/DRE.
- **Sublocacao (art. 3o):** qualquer das partes tem legitimidade para propor a renovacao da locacao/sublocacao; vedada a exclusao de uma delas, salvo inadimplencia.

### 5. Travas transversais
- **Padrao da rede:** o cessionario/renovado segue o DNA (manuais) e o uso correto da marca.
- **Coerencia:** taxas e base de calculo coerentes com COF/contrato/DRE.

## Entrega obrigatoria final
- Para transferencia/cessao: instrumento de cessao com anuencia do franqueador + checklist (perfil do cessionario, quitacao de pendencias, sublocacao, taxa de transferencia). Para sucessao: aditivo de habilitacao do herdeiro/espolio conforme XVII. Para renovacao: aditivo de renovacao / novo contrato com prazo, condicoes (XXII), taxa e revisao de taxas coerente.

## Guard
Nenhum dispositivo sem `validador-franquia`. Numeros (taxas de transferencia/renovacao) so do que a COF/contrato preveem — referencia de mercado e 🟡, nunca lei. Jurisprudencia so apos `varredura-jurisprudencial-pre-tese`. Coerencia COF/contrato/DRE. Marca -> `marca-inpi-adv-os`. Entrega fecha pela `suprema-corte-franchising`.
