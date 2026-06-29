---
description: Porta unica do plugin: classifica a demanda de franquia e conduz todas as skills ate o fechamento.
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

Voce foi acionado pelo `/franchising-master`.

Argumento: `$ARGUMENTS`

**Protocolo:** acionar a skill `franchising-master` — orquestrador que classifica via `triagem-franchising`, carrega `memoria-de-caso-franquia`, seleciona e conduz as skills da tarefa, passa pela gestao (competencia/foro/arbitragem) e fecha pela `suprema-corte-franchising`.

**Skill a acionar:** `franchising-master`.
