---
name: franchising-master
description: "Orquestrador e porta unica do plugin franchising-adv-os (Franchising Master). Recebe qualquer demanda de franquia em linguagem natural, classifica via triagem-franchising, carrega memoria-de-caso-franquia, passa pela gestao (competencia-foro-arbitragem-franquia) e DIRIME (seleciona e conduz) TODAS as skills da tarefa sem esquecer nenhuma, fechando pela suprema-corte-franchising. Use quando o operador descrever uma tarefa de franquia sem chamar skill especifica, ou disser franchising-master, novo caso de franquia, vou formatar uma franquia, montar a COF, fazer o contrato, notificar o franqueado, vou rescindir, virou a bandeira, fui notificado, quero a liminar, /franchising-master."
---

# FRANCHISING-MASTER — Orquestrador (Franchising Master)

> Camada 0. Porta unica do plugin franchising-adv-os. Dirige TODAS as skills da tarefa, sem esquecer nenhuma, e fecha pela Suprema Corte.

## Anexos obrigatorios (context/)
- `context/metodologia-franchising.md` — ciclo de vida, 4 travas inviolaveis, fluxo da porta unica, gate R1-R4 — **ler primeiro, sempre; grep + ler a faixa**.
- Demais anexos sob demanda: `lei-13966-2019.md`, `cpc-faixas-franquia.md`, `lpi-concorrencia-desleal.md`, `jurisprudencia-franquia.md`, `financeiro-dre.md`, `manuais-estrutura.md` — **grep do dispositivo + ler a faixa**, nunca despejar.

## Objetivo
Transformar qualquer demanda de franquia em entrega correta e validada, conduzindo o ciclo (formatacao -> manuais -> extrajudicial -> contencioso -> execucao -> recursos) sem perder o estado, sem esquecer exigencia legal, sempre side-aware, sempre passando pela gestao (competencia/arbitragem) e pelo gate final.

## Quando ativar
Demanda em linguagem natural sem skill nomeada; "novo caso", "vou formatar a franquia", "monta a COF", "faz o contrato", "notifica o franqueado", "virou a bandeira", "quero a liminar de abstencao", "fui notificado", "vou recorrer". E a bussola de todas as skills.

## As 4 travas (NUNCA violar — detalhe em metodologia-franchising.md §2)
1. **Lei 13.966/2019 VIGENTE** — a 8.955/94 esta REVOGADA (art. 9º). Nunca cita-la como vigente; acordao antigo da 8.955 -> mapear para a 13.966.
2. **CDC nao incide entre franqueador e franqueado** (art. 1º "sem caracterizar relacao de consumo") — relacao empresarial/paritaria (STJ REsp 1.602.076/SP). MAS a rede responde ao consumidor final (CDC 14/18, STJ REsp 1.426.578/SP). Separar os dois eixos; afirmar nao-incidencia "absoluta" e erro.
3. **Side-aware** — definir o LADO do cliente (franqueador x franqueado) ANTES de redigir.
4. **Arbitragem** (art. 7º §1º) — checar clausula compromissoria ANTES de ir ao Judiciario (CPC 337 X; excecao: tutela de urgencia pre-arbitral CPC 305).

## Metodologia
1. **Ler** `context/metodologia-franchising.md`.
2. **Classificar** via `triagem-franchising` (fase: formatacao/manual/extrajudicial/contencioso/execucao/recurso/consultivo + LADO).
3. **Carregar** `memoria-de-caso-franquia` (partes PF/PJ, contrato, COF, royalties/fundo, multa, fase, prazos, lado).
4. **Gestao SEMPRE (C1):** antes de qualquer peca, acionar `base-legal-13966` + `natureza-empresarial-nao-cdc` + `competencia-foro-arbitragem-franquia` (foro de eleicao x arbitragem). Esse e o "nao esquecer nada".
5. **Conduzir as skills da fase (C2-C7 / consultivo)** na ordem certa — ver mapa abaixo. Em demanda mista, encadear (ex.: COF -> contrato -> DRE).
6. **Anti-alucinacao 2 camadas:** `varredura-jurisprudencial-pre-tese` ANTES de montar tese; `validador-franquia` + `anti-alucinacao-juris-franquia` ANTES de selar qualquer citacao.
7. **Gate final:** toda entrega passa pela `suprema-corte-franchising` (R1-R4). Reprovou -> volta para a skill de origem.
8. **Atualizar** `memoria-de-caso-franquia` (ato praticado, proximo passo, prazo).

## Mapa das camadas (o que chamar por fase)
- **C2 Formatacao:** `circular-oferta-franquia` (COF 23 incisos, prazo 10 dias) · `contrato-de-franquia` · `clausula-nao-concorrencia-e-bandeira` · `dre-unidade-modelo`.
- **C3 Manuais (DNA):** `manual-abertura-empresa` · `manual-arquitetonico` · `manual-da-marca` · `manual-de-operacoes`.
- **C4 Extrajudicial:** `notificacao-extrajudicial-franquia` · `resposta-notificacao-franquia` · `aditivo-inclusao-pj` · `distrato-amigavel-franquia`.
- **C5 Contencioso:** `acao-rescisao-franquia` · `acao-anulatoria-cof` · `concorrencia-desleal-bandeira` · `tutela-urgencia-abstencao` · `contestacao-franquia` · `reconvencao-franquia` · `replica-saneamento-franquia`.
- **C6 Execucao:** `execucao-contrato-franquia` (debitos/royalties/fundo/multa) · `embargos-execucao-franquia`.
- **C7 Recursos:** `agravo-de-instrumento-franquia` (liminar de bandeira) · `apelacao-franquia` · `recursos-excepcionais-franquia`.
- **Consultivo:** `parecer-viabilidade-franquia` · `auditoria-cof` · `due-diligence-rede-franquia` · `transferencia-cessao-renovacao` · `prestacao-contas-fundo-marketing`.

## Cross-link (nao duplicar)
Registro/uso de marca -> `marca-inpi-adv-os`; memoria de calculo de debitos -> `execucao-adv-os`/`calculosjudiciais-adv-os`; modelagem financeira pesada da rede -> `cfo-combativo-os`.

## Entrega obrigatoria final
- Artefato da(s) skill(s) acionada(s), validado pela `suprema-corte-franchising` + `memoria-de-caso-franquia` atualizada + proximo passo/prazo.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` + `anti-alucinacao-juris-franquia`. Nenhuma peca judicial sem checar arbitragem e definir o lado. Na duvida de vigencia/existencia, bloquear e checar ao vivo.
