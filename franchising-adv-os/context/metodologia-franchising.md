# Metodologia — franchising-adv-os (Franchising Master)

> **Para:** `franchising-onboarding` (explica o plugin ao usuário) + todas as skills (citam este anexo para o **método**).
> **O que é:** o manual de operação do próprio plugin — o que ele faz, como pensa, o que nunca erra e por onde uma demanda flui. Escrito para advogado: claro, sem rodeio.
> **Base normativa:** Lei 13.966/2019 (`lei-13966-2019.md`), LPI 9.279/96 (`lpi-concorrencia-desleal.md`), CPC (faixas), jurisprudência verificada (`jurisprudencia-franquia.md`), modelagem financeira (`financeiro-dre.md`) e estrutura de manuais (`manuais-estrutura.md`).

---

## 1. O QUE O PLUGIN FAZ — o ciclo de vida da franquia

O `franchising-adv-os` é o **sistema operacional do advogado de franchising**. Ele cobre a franquia **de ponta a ponta**, na ordem em que a vida real acontece: monta a franquia, documenta o DNA, tenta resolver fora do tribunal, litiga quando precisa, executa o que ficou devido e recorre até as cortes superiores.

```
FORMATAÇÃO → MANUAIS (DNA) → EXTRAJUDICIAL → CONTENCIOSO → EXECUÇÃO → RECURSOS
```

| Fase | O que o plugin entrega | Skills-núcleo |
|------|------------------------|---------------|
| **1. Formatação** | A franquia "montada": **COF** (23 incisos do art. 2º), **contrato de franquia** empresarial (royalties, fundo, território, não-concorrência, bandeira, multa, foro/arbitragem) e **DRE da unidade-modelo** | `circular-oferta-franquia` · `contrato-de-franquia` · `clausula-nao-concorrencia-e-bandeira` · `dre-unidade-modelo` |
| **2. Manuais (DNA)** | O know-how no papel: **abertura da empresa**, **arquitetônico** (premissas, não o projeto), **marca** (brand book) e **operações** (a operação ponta-a-ponta) | `manual-abertura-empresa` · `manual-arquitetonico` · `manual-da-marca` · `manual-de-operacoes` |
| **3. Extrajudicial** | A tentativa fora do tribunal, **dos dois lados**: notificar/responder, **aditivo de inclusão da PJ**, **distrato amigável** | `notificacao-extrajudicial-franquia` · `resposta-notificacao-franquia` · `aditivo-inclusao-pj` · `distrato-amigavel-franquia` |
| **4. Contencioso** | A peça judicial: **rescisão + multa + não-concorrência**, **anulatória de COF**, **concorrência desleal/bandeira (com liminar)**, **contestação** e **reconvenção** side-aware | `acao-rescisao-franquia` · `acao-anulatoria-cof` · `concorrencia-desleal-bandeira` · `tutela-urgencia-abstencao` · `contestacao-franquia` · `reconvencao-franquia` |
| **5. Execução** | A cobrança do título: **débitos do contrato, royalties, fundo de marketing e multa**; defesa do executado por **embargos** | `execucao-contrato-franquia` · `embargos-execucao-franquia` |
| **6. Recursos** | Subida da causa: **agravo de instrumento** (crítico contra a liminar de bandeira), **apelação**, **REsp** e **RE** | `agravo-de-instrumento-franquia` · `apelacao-franquia` · `recursos-excepcionais-franquia` |

> **Diferencial consultivo (completam o ciclo):** `parecer-viabilidade-franquia` (o negócio pode virar franquia?), `auditoria-cof` (audita a COF de terceiro **antes** de o franqueado assinar), `due-diligence-rede-franquia` (avalia a rede antes da compra), `transferencia-cessao-renovacao` e `prestacao-contas-fundo-marketing`.

> **Fronteiras (cross-link, não duplicar):** `marca-inpi-adv-os` (registro/uso da marca — art. 1º §1º e art. 8º remetem à PI) · `execucao-adv-os` / `calculosjudiciais-adv-os` (memória de cálculo de débitos) · `cfo-combativo-os` (modelagem financeira pesada da rede). O DRE aqui é só o do **modelo de unidade**, não a contabilidade da rede. **Fora do escopo:** relação de consumo (não há — art. 1º) e relação trabalhista do franqueado (não há vínculo — art. 1º).

---

## 2. PREMISSAS INVIOLÁVEIS (o que o plugin NUNCA erra)

Estas quatro travas governam toda peça. Violar qualquer uma é defeito grave.

### 2.1 Lei 13.966/2019 VIGENTE — NUNCA a 8.955/94
A fundação é a **Lei 13.966/2019**. A Lei 8.955/94 está **REVOGADA** (art. 9º da lei nova). Jamais citá-la como vigente. Acórdãos antigos aplicam a 8.955/94 (contratos da época) — ao usá-los, **mapear para os artigos da 13.966/2019** (ex.: a sanção do art. 2º §2º fala em valores "corrigidos monetariamente").

### 2.2 CDC NÃO incide entre franqueador e franqueado — mas a rede responde ao consumidor final
A não-incidência do CDC **está na letra da lei** (art. 1º: *"sem caracterizar relação de consumo"*), não só na jurisprudência. A franquia é relação **empresarial/paritária** (STJ REsp 1.602.076/SP; 632.958/AL). Consequências práticas: **foro de eleição válido**, **sem inversão do ônus da prova**, **sem hipossuficiência presumida**.

**Distinção crítica — dois eixos:**
- **(a) franqueador × franqueado** = empresarial/paritário, **SEM CDC**.
- **(b) rede × consumidor final** (terceiro) = **relação de consumo, COM** responsabilidade solidária da franqueadora (CDC 14/18 — STJ REsp 1.426.578/SP).

Afirmar a não-incidência do CDC "de forma absoluta" é **erro**. O plugin sempre separa os dois eixos.

### 2.3 Side-aware — todo canal tem dois sentidos
Notificação, resposta, contestação, reconvenção, execução e embargos operam **dos dois lados** (franqueador ⇄ franqueado). A primeira coisa que o plugin define é **o lado do cliente**; a peça é construída a partir disso. (Skills de formatação e manuais também mudam de foco conforme o lado: montar a rede ≠ auditar a COF de terceiro antes de assinar.)

### 2.4 Arbitragem — verificar antes de litigar
A Lei 13.966/2019 (**art. 7º §1º**) autoriza cláusula compromissória de arbitragem, **comum** em franquia. Havendo cláusula válida, o Judiciário é **incompetente** (CPC 337 X) — salvo **tutela de urgência pré-arbitral** (CPC 305). Atenção: sendo a franquia contrato de adesão, a cláusula arbitral deve observar o **art. 4º §2º da Lei 9.307/96** (destaque/visto do aderente), sob pena de nulidade (STJ REsp 1.602.076/SP). **Nenhuma peça judicial sai sem checar se há arbitragem.**

> **Resumo das travas:** lei vigente é a 13.966/2019 · CDC só no eixo do consumidor final · lado definido antes de redigir · arbitragem checada antes de ir ao Judiciário.

---

## 3. FLUXO DA PORTA ÚNICA

Toda demanda entra por uma porta só e sai por um portão só. Nada pula etapa.

```
                       ┌──────────────────────────┐
   usuário  ─────────► │   franchising-master      │  (orquestrador — a bússola)
                       └────────────┬─────────────┘
                                    │ 1) classifica a demanda
                                    ▼
                       ┌──────────────────────────┐
                       │   triagem-franchising      │  fase? (formatação / manual /
                       └────────────┬─────────────┘  extrajudicial / contencioso /
                                    │ + LADO          execução / recurso) + lado
                                    ▼
                       ┌──────────────────────────┐
                       │  memoria-de-caso-franquia  │  carrega/atualiza o estado do caso
                       └────────────┬─────────────┘  (partes PF/PJ, contrato, COF,
                                    │                  royalties/fundo, fase, prazos)
                                    ▼
                       ┌──────────────────────────┐
                       │  C1 GESTÃO (sempre)        │  base-legal-13966 ·
                       │  competência / foro /      │  natureza-empresarial-nao-cdc ·
                       │  ARBITRAGEM                 │  competencia-foro-arbitragem
                       └────────────┬─────────────┘
                                    ▼
                       ┌──────────────────────────┐
                       │   SKILL(S) DA FASE          │  C2 a C7 conforme a triagem
                       │   (side-aware)              │  (uma ou várias, conduzidas
                       └────────────┬─────────────┘  pelo master)
                                    ▼
                       ┌──────────────────────────┐
                       │  suprema-corte-franchising │  GATE FINAL R1-R4 (obrigatório)
                       └────────────┬─────────────┘
                                    ▼
                                 entrega
```

**Regras do fluxo:**
1. **`franchising-master` dirime TODAS as skills** pertinentes à tarefa — não esquece nenhuma. Nada vira peça sem passar pela **gestão** (competência/foro/arbitragem) da C1.
2. **`triagem-franchising`** classifica a fase **e o lado**, e roteia. Em demanda mista (ex.: "formata a COF e já me deixa pronto o contrato"), o master encadeia as skills na ordem certa.
3. **`memoria-de-caso-franquia`** mantém o estado: quem é PF e quem é PJ, qual o contrato/COF, base de royalties/fundo, fase processual e prazos. Garante coerência entre peças do mesmo caso.
4. **Gate Suprema Corte é inegociável** — nenhuma entrega escapa dele (§4).

---

## 4. O GATE SUPREMA CORTE (R1–R4)

`suprema-corte-franchising` é a **auditoria final de excelência**, default-on. Toda entrega passa pelos quatro rounds:

| Round | Audita |
|-------|--------|
| **R1 — Fatos / partes / lado / competência** | Partes corretas (PF × PJ)? Lado certo (franqueador × franqueado)? **Há cláusula de arbitragem?** Competência/foro corretos? |
| **R2 — Fundamentação** | Está na **Lei 13.966/2019 vigente** (nunca 8.955/94)? CDC tratado nos dois eixos corretos? Dispositivos certos do CPC/CC/LPI? |
| **R3 — Jurisprudência real** | Toda citação (TJSP/STJ/STF) **existe e está vigente**? Confere com `jurisprudencia-franquia.md` e foi verificada ao vivo? |
| **R4 — Forma / pedidos** | Pedidos completos e coerentes? **Multa** bem fundamentada (CC 413)? **Liminar** com base e periculum (CPC 300 / LPI 209 §1º)? Valor da causa correto? Astreintes (CPC 537)? |

> Se qualquer round reprova, a peça **volta** para a skill responsável antes de ser entregue.

---

## 5. ANTI-ALUCINAÇÃO (R-FRANQUIA — duas camadas)

A camada mais sensível é a jurisprudência. O plugin opera com **duas camadas** de defesa, além do gate R3:

### Camada 1 — `varredura-jurisprudencial-pre-tese` (ANTES de redigir)
Antes de montar a tese, varre **TJSP/STJ/STF na fonte** para confirmar que o entendimento **atual** sustenta o argumento. Mitiga improcedência por tese desatualizada. É proativa: roda antes, não depois.

### Camada 2 — `validador-franquia` + `anti-alucinacao-juris-franquia` (ANTES de selar)
Cruza **cada dispositivo e cada julgado** com o `context/` e com o guard global de anti-alucinação. **Nenhuma citação recebe selo sem verificação real** (a URL/fonte tem de retornar a decisão e o trecho). Na dúvida, **bloqueia e checa ao vivo**.

**Invioláveis R-FRANQUIA:**
- Nenhuma súmula/tese/acórdão/REsp/RE entra sem **verificação real** na fonte.
- **NUNCA** tratar franquia como relação de consumo entre franqueador e franqueado; **NUNCA** citar a Lei 8.955/94 como vigente.
- No financeiro: **nunca cravar número inventado** — o DRE estrutura sobre os dados reais do operador; **projeção ≠ promessa de lucro** (ver `financeiro-dre.md`).
- Benchmarks de mercado (taxas, payback, margens) entram só como **referência 🟡**, nunca como lei.
- Os achados **🟡** do `jurisprudencia-franquia.md` ("⚠️ Confirmar inteiro teor") só viram munição **depois** de abertos na fonte oficial.

---

## 6. COMO O ONBOARDING APRESENTA O PLUGIN

`franchising-onboarding` (comando `/start-franchising`, com botões `AskUserQuestion`) configura o escritório do usuário e explica, em linguagem simples:
- **O que o plugin cobre:** o ciclo de vida da franquia (§1) — "da montagem da rede ao recurso no STJ".
- **O lado preferencial:** o escritório atende **franqueador**, **franqueado** ou **ambos**? (Define o default side-aware.)
- **O tom e o perfil** do escritório (para personalizar peças e comunicação).
- **As travas** que protegem o cliente: lei vigente, CDC só no eixo do consumidor, arbitragem checada, jurisprudência sempre verificada (§2 e §5).

Depois do onboarding, o usuário fala naturalmente o que precisa; a **porta única** (`franchising-master` → `triagem-franchising`) cuida do roteamento.

---

> **Em uma frase:** o `franchising-adv-os` formata, documenta, negocia, litiga, executa e recorre na franquia brasileira — sempre sob a **Lei 13.966/2019**, sempre **side-aware**, sempre passando pela **gestão de competência/arbitragem** e pelo **gate Suprema Corte**, e **nunca** citando jurisprudência sem verificação real nem tratando a franquia como relação de consumo entre as partes.
