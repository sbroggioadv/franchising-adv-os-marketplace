---
name: notificacao-extrajudicial-franquia
description: "Redige notificacao extrajudicial SIDE-AWARE em franquia (identifica o lado ANTES: franqueado->franqueadora OU franqueadora->franqueado). Constitui em mora, aponta o descumprimento (royalties/fundo em atraso, quebra de padrao, uso indevido de marca, falha de suporte/territorio, COF viciada), interpela, fixa prazo para purgar e adverte das medidas (rescisao, execucao do titulo, liminar de abstencao/bandeira, anulatoria). Base = clausulas do contrato + Lei 13.966/2019; prepara o terreno do contencioso/execucao. Use quando o operador disser notificacao extrajudicial, notificar o franqueado, notificar a franqueadora, constituir em mora, interpelar, royalties atrasados, vou avisar antes de processar, /notificacao."
---

# NOTIFICACAO-EXTRAJUDICIAL-FRANQUIA — Notificacao side-aware

> Camada 4 (Extrajudicial). Peca extrajudicial. **Side-aware:** funciona nos dois sentidos (franqueado <-> franqueadora). Define o lado ANTES de redigir.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — base material: royalties/fundo (art. 2º IX), padrao/manuais (XIII), marca (XIV / art. 1º §1º), nao-concorrencia (XV-b/XXI), COF viciada (art. 2º §2º / art. 4º). **grep do inciso.**
- `context/cpc-faixas-franquia.md` — quando a notificacao prepara execucao (CPC 784 III) ou liminar de abstencao (CPC 300 / 305 pre-arbitral). **grep + ler a faixa.**
- `context/lpi-concorrencia-desleal.md` — quando ha uso indevido de marca/bandeira (art. 195 IV/V, 209). **grep.**

## Objetivo
Produzir a notificacao que **constitui em mora**, documenta o inadimplemento, **interpela** a outra parte a sanar em prazo certo e **adverte** das medidas cabiveis — criando prova e marco temporal para o contencioso/execucao, sempre do lado correto do cliente.

## Quando ativar
- Antes de litigar: o cliente quer formalizar a cobranca/exigencia e dar chance de purgar.
- Royalties/fundo em atraso, quebra de padrao, uso indevido da marca, falha de suporte/exclusividade territorial, ou COF viciada a corrigir.

## Metodologia
1. **DEFINIR O LADO (trava side-aware, antes de tudo):**
   - **Franqueadora -> franqueado:** royalties/taxa/fundo em atraso (art. 2º IX-a/c); quebra de padrao operacional/arquitetonico (XIII); uso indevido/descaracterizacao da marca (XIV / art. 1º §1º); cotas minimas (XIX); descumprimento de exclusividade.
   - **Franqueado -> franqueadora:** falha de suporte/supervisao/treinamento prometidos (XIII-a/b/e); violacao de exclusividade territorial (XI); cobranca indevida; **COF omissa/falsa** (art. 2º §2º / art. 4º — exigir correcao/devolucao corrigida de filiacao e royalties).
2. **Carregar `memoria-de-caso-franquia`** (partes PF/PJ, contrato, COF, base de royalties/fundo, valores, fase) e checar via gestao (`competencia-foro-arbitragem-franquia`) se ha **clausula de arbitragem** — a notificacao extrajudicial **nao depende** dela, mas a advertencia de medidas deve apontar o foro/arbitragem correto.
3. **Estrutura da notificacao:**
   1. Qualificacao do notificante e do notificado (PF e/ou PJ).
   2. Referencia ao **contrato de franquia** (data, objeto) e a **COF**.
   3. **Exposicao do inadimplemento** — fato a fato, com valores/datas e a **clausula contratual** violada + o dispositivo da **Lei 13.966** que a sustenta.
   4. **Constituicao em mora / interpelacao** — exigencia clara do que deve ser feito (pagar, cessar o uso, sanar a falha, corrigir a COF).
   5. **Prazo para purgar** (prazo do contrato; na omissao, prazo razoavel) com termo inicial expresso.
   6. **Advertencia das medidas** caso nao atendida: rescisao por inadimplemento; **execucao** do titulo (royalties/fundo/multa liquidos — CPC 784 III); **liminar de abstencao/bandeira** + astreintes (uso indevido de marca); **acao anulatoria de COF** + devolucao corrigida (lado franqueado).
   7. Reserva de direitos e ressalva de boa-fe (tentativa de solucao extrajudicial).
4. **Anti-alucinacao:** valores so os reais do caso (nunca cravar numero); nenhuma jurisprudencia/dispositivo sem cruzar o `context/`. Tom firme, tecnico, sem ameaca vazia.

## Cross-check final (obrigatorio)
- `validador-franquia` — cada dispositivo da Lei 13.966/CPC/LPI conferido no `context/`; **nenhuma 8.955/94 como vigente**; CDC fora do eixo franqueador x franqueado.
- `suprema-corte-franchising` (R1-R4) — lado certo? mora bem constituida? prazo e advertencia coerentes? base contratual + legal corretas? Reprovou -> volta.
