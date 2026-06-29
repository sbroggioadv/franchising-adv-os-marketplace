---
name: memoria-de-caso-franquia
description: "Mantem o estado append-only de um caso de franquia — partes (PF/PJ), contrato, COF (foi entregue? quando? respeitou os 10 dias?), royalties/fundo/taxa de franquia/multa, fase, prazos e LADO do cliente. Use quando o operador retomar um caso, perguntar onde paramos, pedir o status, a cronologia ou os prazos, ou quando o franchising-master precisar carregar/atualizar o estado. Tambem ao iniciar caso novo."
---

# MEMORIA-DE-CASO-FRANQUIA

> Camada 0. Registro append-only do caso. O `franchising-master` le no inicio e atualiza no fim de cada ato.

## Anexos obrigatorios (context/)
- `context/metodologia-franchising.md` — fluxo da porta unica e fases — **grep + ler a faixa**.

## Objetivo
Nunca perder o fio do caso: partes (quem e PF, quem e PJ), o contrato e a COF (entrega e prazo), as bases economicas (royalties/fundo/multa), o LADO do cliente, a fase, os prazos que vencem e o proximo passo.

## Quando ativar
Retomar caso, "onde paramos", "status", "cronologia", "quais prazos"; ou quando o `franchising-master` precisa carregar/atualizar o estado; ou ao iniciar caso novo.

## Onde grava
`franchising/casos/<slug-do-caso>.md` no diretorio de trabalho. **Append-only:** cada ato vira nova linha; nunca apaga o anterior.

## Estrutura do arquivo de caso
```markdown
# Caso: <titulo>
## Partes e lado
- Franqueador: <nome/CNPJ> | Franqueado: <nome — PF e/ou PJ; abriu empresa? data>
- LADO do cliente: franqueador / franqueado
## Contrato e COF
- Contrato: <data de assinatura> | prazo/renovacao: <...>
- COF: entregue? <sim/nao> | quando: <data> | respeitou os 10 dias antes (art. 2º §1º)? <sim/nao>
- Arbitragem: ha clausula compromissoria (art. 7º §1º)? <sim/nao> | foro de eleicao: <comarca>
## Bases economicas
- Taxa de franquia: R$ <...> | Royalties: <% / base> | Fundo de marketing: <% / base> | Multa: <valor/clausula>
## Fase
- <formatacao / manual / extrajudicial / contencioso / execucao / recurso / consultivo>
## Prazos
- <data fatal> | <ato> | <fonte: notificacao/intimacao/publicacao> | dias uteis
## Historico (append-only)
- <data> | <ato praticado> | <skill> | <resultado>
## Proximo passo
- <acao> ate <data>
```

## Metodologia
1. Ao iniciar: criar o arquivo com partes/lado + contrato/COF + bases economicas + fase.
2. A cada ato: **acrescentar** linha no Historico + atualizar Fase/Prazos/Proximo passo.
3. Nunca sobrescrever historico (auditabilidade).

## Entrega obrigatoria final
- Arquivo de caso criado/atualizado + resumo do estado (lado, fase, proximo prazo, pendencias).

## Guard
Estado e fato, nao opiniao. Registrar numeros/datas/prazos exatamente como constam na fonte (contrato/COF/notificacao/intimacao); prazos em dias uteis — nao estimar datas sem o marco. **A data de entrega da COF e o respeito aos 10 dias sao fatos-chave** (sustentam ou afastam a anulatoria) — registrar com a fonte.
