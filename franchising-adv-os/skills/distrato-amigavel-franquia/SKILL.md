---
name: distrato-amigavel-franquia
description: "Redige o instrumento de DISTRATO amigavel da franquia, aplicando as proprias clausulas do contrato (depende do acordo das partes). Cobre quitacao reciproca (com ou sem ressalvas), acerto de valores em aberto (royalties/fundo/multa), destino do estoque, do ponto comercial e da sublocacao (art. 3º), DESBANDEIRAMENTO (devolucao/retirada de materiais de marca, fachada e sistema), prazo da nao-concorrencia remanescente (XV-b/XXI), confidencialidade e cronograma de encerramento. Base = clausulas do contrato + Lei 13.966/2019. Use quando o operador disser distrato, encerrar a franquia de forma amigavel, rescisao consensual, sair da rede em acordo, desbandeirar, devolver a loja, encerrar o contrato sem briga, /distrato."
---

# DISTRATO-AMIGAVEL-FRANQUIA — Distrato consensual

> Camada 4 (Extrajudicial). Instrumento contratual extrajudicial. **Depende do acordo das partes** — gera o instrumento que encerra a relacao aplicando as clausulas do proprio contrato.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — **art. 2º XV-b** (atividade concorrente pos-contrato) e **XXI** (limitacao a concorrencia), **art. 3º** (sublocacao do ponto), **art. 1º §1º** (titularidade da marca -> desbandeiramento). **grep do inciso.**
- `context/lpi-concorrencia-desleal.md` — uso pos-rescisao da marca/insignia (art. 195 IV/V/XI) — base para a clausula de retirada da bandeira. **grep.**

## Objetivo
Produzir o **distrato** que desfaz a franquia de forma **consensual e organizada**, fechando todas as pontas: quitacao, valores, estoque, ponto, **desbandeiramento** (retirada da marca/fachada/sistema), nao-concorrencia remanescente, confidencialidade e cronograma — prevenindo o litigio que o "virar a bandeira" costuma gerar.

## Quando ativar
- Ambas as partes querem encerrar a relacao em acordo (franqueador e franqueado de comum acordo).
- Contraproposta de encerramento surgida na fase de notificacao/resposta (-> `resposta-notificacao-franquia`).

## Metodologia
1. **Confirmar o acordo e o lado:** distrato exige consenso; mapear o que cada parte quer (valores, prazos, estoque, ponto). Carregar `memoria-de-caso-franquia` e ler as clausulas do contrato que regem o encerramento.
2. **Acertar os pontos materiais (checklist do distrato):**
   - **Acerto de valores em aberto** — royalties, fundo, taxas, multa; forma de pagamento/parcelamento; eventual desconto negociado.
   - **Estoque** — destino (recompra pela franqueadora, venda esgotamento por prazo certo, devolucao), inclusive itens com a marca.
   - **Ponto comercial / sublocacao (art. 3º)** — quem fica com o ponto; encerramento ou cessao da locacao/sublocacao; chaves e benfeitorias.
   - **Desbandeiramento** — prazo e responsavel pela **retirada de fachada, comunicacao visual, uniformes, materiais e do sistema/acesso**; vedacao de uso da marca/insignia apos a data (art. 1º §1º; LPI art. 195 IV/V/XI) — previne o `concorrencia-desleal-bandeira`.
   - **Nao-concorrencia remanescente** — confirmar se subsiste a restricao pos-contratual (XV-b/XXI) e com que **limites validos (prazo + territorio)**; nao pode impedir o exercicio da atividade economica em si.
   - **Confidencialidade/know-how** — mantida apos o distrato (LPI art. 195 XI: "mesmo apos o termino do contrato").
3. **Clausulas do instrumento:**
   1. Preambulo (qualificacao das partes — PF/PJ — e referencia ao contrato).
   2. **Resolucao consensual** do contrato a partir de data certa.
   3. Acerto de valores + comprovacao/cronograma de pagamento.
   4. Estoque, ponto/sublocacao e **desbandeiramento** (com prazos e penalidade por atraso).
   5. Nao-concorrencia remanescente e confidencialidade (com limites).
   6. **Quitacao** — reciproca e geral, OU **com ressalvas** expressas (preservar pretensoes nao abrangidas). Definir o alcance com cuidado.
   7. Cronograma de encerramento (entrega de chaves, retirada de marca, baixa de acessos) e foro/arbitragem para o que sobrar (art. 7º §1º).
   8. Assinaturas (partes + 2 testemunhas).
4. **Anti-alucinacao:** valores reais do caso; quitacao geral so com ciencia do cliente do que esta abrindo mao; nao-concorrencia sempre com limites (prazo+territorio).

## Cross-check final (obrigatorio)
- `validador-franquia` — dispositivos da Lei 13.966 (art. 2º XV-b/XXI, art. 3º, art. 1º §1º, art. 7º) e LPI (195) conferidos no `context/`; **nenhuma 8.955/94 como vigente**; CDC fora do eixo franqueador x franqueado.
- `suprema-corte-franchising` (R1-R4) — acordo completo? desbandeiramento e nao-concorrencia com limites validos? quitacao com alcance correto (geral x com ressalvas)? Reprovou -> volta.
