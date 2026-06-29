---
name: manual-abertura-empresa
description: "Formata o Manual de Abertura/Implantacao da unidade franqueada: passo a passo para 'ligar' a loja — constituicao da PJ (tipo societario MEI/ME/EPP/SLU/LTDA, contrato social, CNAE), CNPJ, inscricoes estadual/municipal, enquadramento tributario (Simples x Presumido x Real — VARIAVEL pela Reforma Tributaria, nunca cravar aliquota), licencas (alvara/vigilancia/bombeiros/ambiental), conta PJ, ponto comercial e cronograma de implantacao (Gantt). Da lastro a COF (art. 2º VIII/XIII/XIII-g) e liga ao aditivo-inclusao-pj. Use quando o operador disser manual de abertura, manual de implantacao, como abrir a empresa do franqueado, constituir a PJ da unidade, cronograma de implantacao, que licencas a unidade precisa, enquadramento tributario da franquia, /manual abertura."
---

# MANUAL-ABERTURA-EMPRESA — Manual de Implantacao da unidade

> Camada 3 (Manuais / DNA). Consultoria de negocio/formatacao: estrutura o manual que ensina o franqueado a "ligar" a unidade. Nao redige peca judicial.

## Anexos obrigatorios (context/)
- `context/manuais-estrutura.md` — secao **1** (Manual de Abertura/Implantacao): objetivo, indice, checklist, conexao COF. **grep + ler a faixa.**
- `context/lei-13966-2019.md` — art. 2º **VIII** (investimento inicial), **XIII-g** (ponto), **art. 3º** (sublocacao), **art. 4º** (promessa sem lastro). **grep do inciso.**

## Objetivo
Estruturar o **Manual de Abertura/Implantacao**: o passo a passo, do contrato assinado a inauguracao, cobrindo (a) a constituicao juridico-formal da PJ e (b) o cronograma fisico de montagem da unidade. E o manual que da seguranca no momento de maior investimento do franqueado e que sustenta o `aditivo-inclusao-pj` (o franqueado compra na **pessoa fisica**, abre a empresa por este manual e adita o contrato para incluir a PJ).

## Quando ativar
- Montar/revisar o manual de implantacao da rede (lado franqueador).
- O operador pergunta como abrir a empresa do franqueado, que tipo societario/regime/licencas, ou pede o cronograma de implantacao.

## Metodologia
1. **Ler a secao 1 de `manuais-estrutura.md`.** Principio: o manual transforma know-how tacito em processo replicavel — **escrever para quem NAO sabe**, literal e visual (Gantt, checklists).
2. **Indice de capitulos (montar todos):**
   1. Visao geral e prazo total da implantacao (fases e estimativa).
   2. **Cronograma (Gantt)** — etapas, dependencias, responsavel (franqueado x franqueadora), marcos.
   3. **Constituicao da PJ** — tipo societario (MEI/ME/EPP/SLU/LTDA conforme faturamento previsto, nº de socios, protecao patrimonial) 🔴 *a SLU substituiu a EIRELI; confirmar limites vigentes antes de afirmar valores*; CNAE principal + secundarios; contrato social/requerimento de empresario; documentos dos socios + certificado digital (e-CNPJ/e-CPF).
   4. **Registros e inscricoes** — viabilidade previa (prefeitura), Junta Comercial (Redesim, digital), CNPJ (Receita), Inscricao Estadual (SEFAZ — vende produto/ICMS), Inscricao Municipal/CCM (servico/ISS).
   5. **Enquadramento tributario** — Simples Nacional x Lucro Presumido x Lucro Real (criterio por faturamento/margem/folha, fator R). 🔴 **VARIAVEL** — faixas e aliquotas mudam (Reforma Tributaria: CBS substitui PIS/COFINS, IBS substitui ICMS/ISS, em transicao); tratar como **dado datado, NUNCA hardcode**; "consulte seu contador".
   6. **Licencas e alvaras** — alvara de funcionamento; Vigilancia Sanitaria (alimentacao/saude/estetica); Bombeiros (AVCB/CLCB); licenca ambiental quando aplicavel. Atividade de baixo risco -> alvara provisorio/automatico via Redesim.
   7. **Conta PJ** + meios de pagamento (adquirencia) + emissao de NF-e/NFS-e.
   8. **Ponto comercial** — analise/aprovacao pela franqueadora (COF XIII-g), locacao **ou** sublocacao (art. 3º da Lei).
   9. **Obra e montagem** — projeto aprovado (-> `manual-arquitetonico`), reforma, fachada, mobiliario, equipamentos, comunicacao visual.
   10. **Estoque inicial** com fornecedores homologados (COF XII).
   11. **Contratacao/treinamento inicial** da equipe (-> `manual-de-operacoes`).
   12. **Marketing de inauguracao** (-> `manual-da-marca`).
   13. **Checklist de pre-abertura (go/no-go).**
3. **Checklist — o que NAO pode faltar:**
   - [ ] Cronograma com prazo e responsavel por etapa (franqueado x franqueadora).
   - [ ] Arvore de decisao de **tipo societario** e de **regime tributario** (com "nao substitui o contador").
   - [ ] Lista de **licencas por tipo de atividade/segmento**.
   - [ ] Documentacao necessaria consolidada em lista unica.
   - [ ] Lista de **fornecedores homologados** do estoque inicial (amarra COF XII).
   - [ ] **Checklist de pre-abertura** (alvara emitido? padrao arquitetonico auditado? equipe treinada? estoque conferido?).
   - [ ] Contatos/canais de **suporte da franqueadora** na implantacao.
4. **Conexao COF/contrato:** COF **VIII** (investimento inicial estimado) — o manual operacionaliza onde o dinheiro vai; COF **XIII-g** + **art. 3º** (ponto/sublocacao). A entrega deste manual integra o **suporte de implantacao** prometido na COF (XIII) e devido pelo contrato — **promessa sem manual = exposicao (art. 4º)**.
5. **Liga ao `aditivo-inclusao-pj`:** o manual ensina a abrir a PJ; o aditivo formaliza a inclusao da PJ no contrato. Encadear quando o caso for "franqueado ja abriu a empresa".

## Guard
Numeros tributarios/societarios sao **VARIAVEIS** (Reforma Tributaria em transicao) — nunca hardcode, sempre "dado datado + confirme com contador". A ancora legal dura e so a **Lei 13.966/2019** (art. 2º XIII-f manuais). **Nunca citar a 8.955/94 como vigente.**
