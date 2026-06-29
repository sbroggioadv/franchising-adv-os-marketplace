---
name: aditivo-inclusao-pj
description: "Redige o termo aditivo que inclui a PESSOA JURIDICA no contrato de franquia: o franqueado contratou na PESSOA FISICA, abriu a empresa (manual-abertura-empresa) e agora adita o contrato para incluir PF + PJ como contratantes — com solidariedade/garantia pessoal da PF (e, se for o caso, fianca/aval). Cobre clausulas de aditamento, sub-rogacao/assuncao das obrigacoes pela PJ, ratificacao integral do contrato original e anexos, manutencao do prazo/foro/arbitragem. Base = clausulas do contrato + Lei 13.966/2019 (XVII transferencia, art. 7º). Use quando o operador disser aditivo de inclusao da PJ, incluir a empresa no contrato, franqueado abriu a PJ, passar o contrato para a pessoa juridica, aditar o contrato de franquia, /aditivo pj."
---

# ADITIVO-INCLUSAO-PJ — Aditivo de inclusao da pessoa juridica

> Camada 4 (Extrajudicial). Instrumento contratual extrajudicial. Liga ao `manual-abertura-empresa` (o franqueado abriu a PJ por la; aqui se formaliza a inclusao).

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2º XVII** (regras de transferencia/sucessao), **art. 7º** (contrato em portugues + lei BR; §1º arbitragem). **grep do inciso.**
- `context/manuais-estrutura.md` — secao **1** (gancho: o manual ensina a abrir; o aditivo formaliza). **grep.**

## Objetivo
Formalizar a entrada da **PJ** do franqueado no contrato de franquia originalmente firmado pela **PF**, incluindo **PF + PJ como contratantes**, preservando a **responsabilidade pessoal da PF** (solidariedade/garantia) e **ratificando** integralmente o contrato original e seus anexos — sem novar o que nao se quis novar.

## Quando ativar
- O franqueado comprou na pessoa fisica, constituiu a empresa e precisa transferir/estender a operacao para a PJ.
- Reestruturacao societaria do franqueado que mantenha a PF como garantidora.

## Metodologia
1. **Checar a base no contrato e na COF:** existe regra de **transferencia/sucessao** (art. 2º XVII; clausula do contrato)? A franqueadora precisa **anuir** (em regra sim — contrato intuitu personae). O aditivo so se sustenta com a anuencia da franqueadora.
2. **Carregar `memoria-de-caso-franquia`** (quem e a PF, dados da PJ ja constituida — CNPJ, socios, capital) e checar arbitragem/foro (`competencia-foro-arbitragem-franquia`) para **manter** a clausula original.
3. **Definir a estrutura juridica da inclusao:**
   - **Inclusao cumulativa** (recomendada): PF **e** PJ passam a figurar como contratantes; a PF permanece **solidariamente** responsavel/garantidora das obrigacoes (royalties, fundo, multa) — protege a franqueadora.
   - **Assuncao pela PJ** das obrigacoes operacionais, **sem liberar** a PF (sem novacao subjetiva liberatoria, salvo se expressamente pactuada).
   - Garantias pessoais (aval/fianca/garantia) da PF e/ou socios, se previstas.
4. **Clausulas do termo aditivo:**
   1. Preambulo — qualificacao da franqueadora, da PF (franqueado original) e da PJ (novo contratante), com referencia ao contrato original (data, objeto).
   2. **Objeto do aditivo** — inclusao da PJ no polo de franqueado.
   3. **Solidariedade/garantia da PF** — a PF responde solidariamente; manutencao de garantias.
   4. **Assuncao de obrigacoes pela PJ** (operacao, padrao, pagamentos) e **vinculacao aos manuais** vigentes.
   5. **Ratificacao** integral do contrato original e anexos no que nao for expressamente alterado.
   6. **Manutencao** de prazo, royalties/fundo, territorio, nao-concorrencia, **foro/arbitragem** (art. 7º §1º) e demais clausulas.
   7. Declaracoes (regularidade da PJ, ausencia de impedimento) e data/assinaturas (franqueadora + PF + PJ + 2 testemunhas — preserva forca de titulo, CPC 784 III).
5. **Anti-alucinacao:** nao inventar clausula que o contrato original nao tem; nao criar novacao nao desejada; dados da PJ sao os reais do caso.

## Cross-check final (obrigatorio)
- `validador-franquia` — dispositivos da Lei 13.966 (art. 2º XVII, art. 7º) conferidos no `context/`; **nenhuma 8.955/94 como vigente**; CDC fora do eixo franqueador x franqueado.
- `suprema-corte-franchising` (R1-R4) — partes corretas (PF + PJ)? Solidariedade preservada? Ratificacao sem novacao indevida? Foro/arbitragem mantidos? Reprovou -> volta.
