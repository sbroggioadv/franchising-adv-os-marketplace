---
name: franchising-onboarding
description: "Wizard de configuracao do plugin franchising ao perfil do escritorio. Cria a pasta franchising/ com identidade (nome, OAB, escritorio, cidade, e-mail), lado preferencial (atende franqueador? franqueado? ambos?), areas de atuacao (formatacao/contencioso/ambos), tom e modo de fluxo. Usa context/metodologia-franchising.md para explicar o que o plugin faz. Use quando o operador disser configurar franchising, instalar franchising, primeira vez, /start-franchising, onboarding franquia."
---

> **🖱️ Escolhas = botoes:** em campos de **lista fechada** (lado preferencial, areas de atuacao, tom, modo de fluxo, atualizar/recriar, sim/nao) use a ferramenta **AskUserQuestion** para mostrar **botoes clicaveis** (max. 4 por pergunta; se houver mais, divida em 2). **Texto livre** (nome, OAB, escritorio, cidade, e-mail) segue como pergunta digitada normal.

# FRANCHISING ONBOARDING

> Camada 0. Wizard de configuracao inicial. Linguagem acolhedora, sem jargao. Configura o plugin ao perfil do escritorio.

## Anexos obrigatorios (context/)
- `context/metodologia-franchising.md` — para explicar o que o plugin faz (ciclo de vida da franquia, travas, side-aware) — **grep + ler a faixa**.

## Objetivo
Configurar o plugin ao escritorio em poucas perguntas e explicar, em linguagem simples, o que ele cobre: o ciclo de vida da franquia ("da montagem da rede ao recurso no STJ"), o lado preferencial e as travas que protegem o cliente.

## Quando ativar
`/start-franchising` ou "configurar franchising", "instalar franchising", "primeira vez", "onboarding franquia". Cria/atualiza `franchising/perfil.md` no diretorio de trabalho.

## Regras do wizard
Uma pergunta por vez, acolhedor. Listas fechadas = AskUserQuestion (botoes). Texto livre = pergunta digitada. Ao fim, gravar e confirmar.

## Blocos de pergunta
1. **Identidade (texto livre):** nome, OAB (nº/UF), escritorio, cidade, e-mail.
2. **Lado preferencial (botoes):** Franqueador (monto/defendo a rede) · Franqueado (compro/defendo a unidade) · Ambos. — define o default side-aware.
3. **Areas de atuacao (botoes, multi):** Formatacao (COF/contrato/DRE/manuais) · Contencioso/extrajudicial (notificacao/acoes/recurso) · Consultivo (viabilidade/auditoria de COF/due diligence) · Tudo.
4. **Tom das pecas (botoes):** Tecnico-formal · Direto e objetivo · Combativo.
5. **Modo de fluxo (botoes):** Checkpoint (confirma a cada etapa) · Continuo.

## Explicacao do plugin (apresentar ao fim, em 4 frases)
- **O que cobre:** formata a franquia (COF dos 23 incisos + contrato + DRE da unidade), documenta o DNA (manuais), negocia fora do tribunal, litiga, executa e recorre.
- **Side-aware:** trabalha dos dois lados — franqueador e franqueado.
- **As travas:** Lei 13.966/2019 vigente (a 8.955/94 esta revogada), CDC so no eixo do consumidor final, arbitragem sempre checada antes de litigar, jurisprudencia sempre verificada.
- **Como usar:** depois daqui, basta falar o que precisa — a porta unica (`franchising-master` -> `triagem-franchising`) cuida do roteamento.

## Gravacao
Criar `franchising/perfil.md`. Se ja existir, perguntar (botoes) Atualizar ou Recriar.

## Entrega obrigatoria final
- `franchising/perfil.md` + resumo da configuracao + sugestao do primeiro comando (`/triagem-franquia` ou `/franchising-master`).

## Guard
Nao inventar dados do operador. O lado preferencial e o default, nao uma trava: o `triagem-franchising` redefine o lado caso por caso.
