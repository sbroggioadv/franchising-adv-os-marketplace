---
name: triagem-franchising
description: "Classifica a demanda de franquia e roteia para as skills certas. Identifica a FASE (formatacao COF/contrato/DRE, manual, extrajudicial, contencioso, execucao, recurso, consultivo) e o LADO (franqueador x franqueado), e indica a skill alvo + a gestao obrigatoria (competencia/foro/arbitragem). Use quando o operador descrever uma situacao de franquia e nao souber o caminho, ou disser triagem franquia, qual o caminho, que peca eu uso, em que fase estou, /triagem-franquia."
---

# TRIAGEM-FRANCHISING

> Camada 0. Porta de classificacao. Chamada pelo `franchising-master` no inicio de todo caso. Define a FASE **e o LADO**.

## Anexos obrigatorios (context/)
- `context/metodologia-franchising.md` — mapa de skills + fluxo da porta unica — **grep + ler a faixa**.
- `context/cpc-faixas-franquia.md` — se a fase for contencioso/execucao/recurso (competencia, rito, tutela).

## Objetivo
Em poucas perguntas, dizer: **fase + LADO + skill(s) alvo + gestao (competencia/foro/arbitragem)** e devolver o handoff para o `franchising-master`.

## Primeira definicao — o LADO (sempre)
O cliente e **franqueador** (monta/defende a rede) ou **franqueado** (compra/defende a unidade)? Toda peca side-aware (notificacao/resposta, contestacao, reconvencao, execucao/embargos) muda conforme isto.

## Tabela de roteamento (fase -> skill alvo)
1. **FORMATACAO** ("vou montar a franquia", "preciso da COF/contrato/DRE") -> `circular-oferta-franquia` (COF 23 incisos + prazo 10 dias) · `contrato-de-franquia` · `clausula-nao-concorrencia-e-bandeira` · `dre-unidade-modelo`. Encadear na ordem COF -> contrato -> clausulas -> DRE.
2. **MANUAL (DNA)** ("manual de operacoes/marca/arquitetonico", "documentar o know-how") -> `manual-abertura-empresa` · `manual-arquitetonico` · `manual-da-marca` · `manual-de-operacoes`.
3. **EXTRAJUDICIAL** ("notificar", "fui notificado", "incluir minha empresa", "encerrar amigavel") -> `notificacao-extrajudicial-franquia` (side-aware) · `resposta-notificacao-franquia` · `aditivo-inclusao-pj` (PF comprou e abriu PJ) · `distrato-amigavel-franquia`.
4. **CONTENCIOSO** ("vou processar/rescindir", "virou a bandeira", "COF era falsa/omissa", "fui citado", "quero liminar") -> rescindir+multa+nao-concorrencia: `acao-rescisao-franquia`; franqueado anula COF deficiente: `acao-anulatoria-cof`; ex-franqueado usa marca/sistema: `concorrencia-desleal-bandeira` + `tutela-urgencia-abstencao`; defesa: `contestacao-franquia` (+ `reconvencao-franquia`); ordenar o processo: `replica-saneamento-franquia`.
5. **EXECUCAO** ("cobrar royalties/fundo/multa por titulo", "fui executado") -> credor: `execucao-contrato-franquia` (debitos/royalties/fundo/multa); executado: `embargos-execucao-franquia`.
6. **RECURSO** ("recorrer", "agravar da liminar", "apelar", "REsp/RE") -> liminar de bandeira (CPC 1.015 I): `agravo-de-instrumento-franquia`; sentenca: `apelacao-franquia`; ultima instancia vs lei federal/CF: `recursos-excepcionais-franquia`.
7. **CONSULTIVO** ("posso virar franquia?", "audita essa COF antes de eu assinar", "vale comprar essa rede?", "transferir/renovar", "prestacao de contas do fundo") -> `parecer-viabilidade-franquia` · `auditoria-cof` · `due-diligence-rede-franquia` · `transferencia-cessao-renovacao` · `prestacao-contas-fundo-marketing`.

## Gestao obrigatoria (sempre, antes da peca)
Toda fase contenciosa/extrajudicial/execucao passa por `base-legal-13966` + `natureza-empresarial-nao-cdc` + `competencia-foro-arbitragem-franquia` (ha clausula de arbitragem? art. 7º §1º).

## Entrega obrigatoria final
- Fase + LADO + skill(s) alvo + gestao, em 3-5 linhas, e o handoff para o `franchising-master`.

## Guard
Na duvida de competencia/foro/arbitragem, apontar `competencia-foro-arbitragem-franquia` antes de redigir. Nao redigir peca aqui — so classificar e rotear. Demanda mista: listar as skills na ordem certa para o master encadear.
