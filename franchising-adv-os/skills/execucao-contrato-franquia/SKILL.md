---
name: execucao-contrato-franquia
description: "Executa o contrato de franquia como titulo executivo extrajudicial (CPC 784 III — contrato assinado pelo devedor + 2 testemunhas; §4o e-assinatura com integridade conferida pelo provedor dispensa as testemunhas), parametrizada pelos 4 OBJETOS: debitos do contrato, royalties, fundo de marketing e multa. Distincao-chave: so executa o LIQUIDO (786 §u — calculo aritmetico nao tira a liquidez); royalties percentuais que dependem de apurar faturamento sao ILIQUIDOS e vao a conhecimento/cobranca (785/803 I). Inicial 798 + demonstrativo discriminado, honorarios 827 (10%, metade em 3 dias), citacao/penhora 829, contraprestacao 787. Use quando o operador disser executar a franquia, cobrar royalties/fundo/multa por execucao, contrato e titulo executivo, executar debitos do franqueado, ja tenho titulo e quero penhorar."
---

# EXECUCAO-CONTRATO-FRANQUIA

> Camada 6 (execucao). Cobranca do que e CERTO, LIQUIDO e EXIGIVEL no contrato de franquia. Lado tipico: **franqueador (exequente)** contra franqueado inadimplente — mas o objeto/calculo e parametrizado e o lado pode inverter. Credito SEM liquidez nao se executa: vai a `acao-anulatoria-cof`? nao — vai a cobranca/conhecimento (CPC 785).

## Anexos obrigatorios (context/)
- `context/cpc-faixas-franquia.md` — **§1 (titulo executivo: 784 III + §4o, 783, 786 §u, 787, 803 I)**, **§3 (execucao por quantia: 798 + §u, 824, 827, 829, 830, 802 prescricao)**, **§2.1 (rito 318)**. `grep -niE "784|786|787|798|827|829|803" context/cpc-faixas-franquia.md`.
- `context/lei-13966-2019.md` — **art. 2o IX-a (royalties), IX-c (fundo), XVIII (multa)**: as 4 verbas nascem aqui.
- `context/financeiro-dre.md` — **§1.2 e §6** base de calculo dos royalties/fundo (a mesma do DRE/COF/contrato) e o que torna a verba liquida ou iliquida.
- `context/jurisprudencia-franquia.md` — **Tema H** (cobranca = prescricao decenal CC 205) e **Tema E (fundo)** — so apos confirmar (achados 🟡).

## Objetivo
Instaurar a execucao por quantia certa sobre o titulo (contrato de franquia), cobrando apenas as verbas **liquidas**, com demonstrativo discriminado e fluxo 827 -> 829 -> penhora — e desviando para cobranca/conhecimento tudo o que for iliquido (sob pena de nulidade, 803 I).

## Quando ativar
- Ha contrato de franquia assinado (titulo) e debitos vencidos: royalties fixos/minimos, taxa, fundo, ou multa contratual com valor/percentual fixo.
- Gatilhos: "executar a franquia", "cobrar royalties por execucao", "fundo de marketing em atraso", "multa do contrato", "ja tenho titulo".

## Metodologia

### 1. Gestao processual SEMPRE (Camada 1)
`competencia-foro-arbitragem-franquia` ANTES de tudo: **ha clausula de arbitragem?** A execucao de titulo extrajudicial corre no **Judiciario** mesmo havendo clausula arbitral (a arbitragem nao tem poder de constricao); mas a discussao de merito do credito pode ser arbitral. Definir foro (CPC 63 + Lei 14.879/2024).

### 2. O titulo — CPC 784 III (verbatim)
> **Art. 784, III** — "o documento particular assinado pelo devedor e por 2 (duas) testemunhas". **§4o** — nos titulos por meio eletronico "e admitida qualquer modalidade de assinatura eletronica prevista em lei, **dispensada a assinatura de testemunhas quando sua integridade for conferida por provedor de assinatura**".

O **contrato de franquia + 2 testemunhas** e titulo executivo extrajudicial. Assinado em plataforma com integridade conferida pelo provedor -> dispensam-se as testemunhas (§4o). **Sem as 2 testemunhas e sem e-assinatura integra, NAO ha titulo** -> cobrança pelo rito comum.

### 3. Filtro de liquidez — o coracao da triagem (parametrizar pelos 4 objetos)
> **Art. 783** — execucao funda-se em obrigacao **certa, liquida e exigivel**. **Art. 786 §u** — "a necessidade de **simples operacoes aritmeticas** para apurar o credito exequendo **nao retira a liquidez**". **Art. 803, I** — "e **nula** a execucao se o titulo nao corresponder a obrigacao certa, liquida e exigivel".

| Objeto (argumento) | Em regra | Caminho |
|---|---|---|
| **debitos do contrato** (taxa/filiacao fixa em atraso) | liquido | execucao |
| **royalties** fixos/minimos ou por calculo aritmetico | liquido (786 §u) | execucao |
| **royalties % sobre faturamento** que dependem de **apurar faturamento** | **iliquido** | **cobranca/conhecimento** (785) |
| **fundo de marketing** com valor/% determinado | liquido | execucao |
| **multa (clausula penal)** com valor/percentual fixo | liquido | execucao |

> **Regra de ouro:** titulo executivo **nao comporta liquidacao** dentro da execucao. Royalties percentuais cujo *quantum* exige instrucao/pericia -> **cobranca pelo rito comum** (CPC 785: "a existencia de titulo executivo extrajudicial nao impede a parte de optar pelo processo de conhecimento"); forçar execucao iliquida = nulidade (803 I). Cross-link `execucao-adv-os` / `calculosjudiciais-adv-os` para memoria de calculo pesada.

### 4. Contraprestacao — CPC 787 (franquia e contrato bilateral)
> **Art. 787** — "se o devedor nao for obrigado a satisfazer sua prestacao senao mediante a **contraprestacao do credor**, este devera **provar que a adimpliu** ao requerer a execucao, sob pena de extincao do processo".

O franqueador-exequente que cobra royalties pode ter de demonstrar que cumpriu suporte/sistema (estrutura sinalagmatica), sob pena de o franqueado opor a *exceptio* (ver `embargos-execucao-franquia`).

### 5. Peticao inicial da execucao — CPC 798 (verbatim §u)
> **Art. 798, I** — instruir com: a) **o titulo** (contrato + testemunhas/e-assinatura); b) **demonstrativo do debito atualizado**; d) prova da contraprestacao (787). **II** — indicar a especie, partes (CPF/CNPJ) e **bens penhoraveis sempre que possivel**. **§u** — o demonstrativo deve conter: I indice de correcao; II taxa de juros; III termos inicial e final; IV periodicidade da capitalizacao; V desconto obrigatorio.

Memoria de calculo discriminada (798 §u) coerente com a **base do DRE/COF/contrato** (financeiro-dre §6). Defeito -> emenda em 15 dias sob pena de indeferimento (801).

### 6. Honorarios e citacao — CPC 827 e 829 (verbatim)
> **Art. 827** — ao despachar, o juiz fixa **honorarios de 10%**; **§1o** integral pagamento em **3 dias** -> honorarios **reduzidos a metade (5%)**; **§2o** ate **20%** se rejeitados os embargos.
> **Art. 829** — executado citado para **pagar em 3 dias**; **§1o** do mandado consta a **ordem de penhora e avaliacao**, cumpridas tao logo verificado o nao pagamento.

Fluxo: despacho 10% (827) -> citacao para pagar em 3 dias (829) -> nao pagou -> **penhora + avaliacao** no mesmo mandado. Executado nao encontrado -> **arresto** (830). O **despacho que ordena a citacao interrompe a prescricao** retroagindo a propositura (802).

### 7. Prescricao da cobranca
Cobranca de valores do contrato (inadimplemento) = **decenal, CC art. 205** (Tema H — fundamento legal vigente; AREsp 2.801.115/PR 🟡 so apos confirmar).

## Entrega obrigatoria final
- Inicial de execucao por quantia certa (798) com o titulo identificado (784 III/§4o), demonstrativo discriminado (798 §u) por objeto, prova da contraprestacao (787), indicacao de bens, pedido de honorarios 827 e citacao 829.
- Triagem explicita liquido x iliquido das 4 verbas; o iliquido roteado a cobranca/conhecimento com nota.

## Guard
Nenhum dispositivo/jurisprudencia sem `validador-franquia` (cruza `context/`). Verba iliquida JAMAIS na execucao (803 I) — desviar. Numeros so do demonstrativo real (base do DRE), nunca inventar. Tema H/E so apos `varredura-jurisprudencial-pre-tese`. Gestao (arbitragem/foro) por `competencia-foro-arbitragem-franquia`. Defesa do executado -> `embargos-execucao-franquia`. Entrega fecha pela `suprema-corte-franchising`.
