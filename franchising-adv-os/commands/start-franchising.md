---
description: Inicia o wizard de configuracao do plugin franchising — perfil do escritorio e lado de atuacao (franqueador/franqueado/ambos).
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

Voce foi acionado pelo `/start-franchising` do plugin franchising-adv-os (Franchising Master).

Argumento: `$ARGUMENTS`

**Protocolo:** acionar a skill `franchising-onboarding` (wizard com botoes via AskUserQuestion nas escolhas de lista fechada). Cria `<cwd>/franchising/perfil.md` (identidade, lado preferencial, areas, tom). Se ja existir, oferecer atualizar/recriar.

**Skill a acionar:** `franchising-onboarding`.
