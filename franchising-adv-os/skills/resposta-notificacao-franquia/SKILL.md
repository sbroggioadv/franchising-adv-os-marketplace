---
name: resposta-notificacao-franquia
description: "Redige a RESPOSTA a uma notificacao extrajudicial recebida em franquia, SIDE-AWARE (identifica o lado do cliente ANTES). Conforme a estrategia: refuta o alegado, reconhece e purga a mora, contrapropoe, registra ressalvas/protestos e prepara o terreno para o contencioso. Cuida do efeito do silencio, da contranotificacao e da prova. Base = clausulas do contrato + Lei 13.966/2019. Use quando o operador disser responder notificacao, fui notificado, recebi uma notificacao do franqueador, recebi notificacao do franqueado, contranotificar, vou rebater a notificacao, /resposta notificacao."
---

# RESPOSTA-NOTIFICACAO-FRANQUIA — Resposta side-aware

> Camada 4 (Extrajudicial). Peca extrajudicial. **Side-aware:** responde do lado do cliente (franqueado OU franqueadora). Define o lado ANTES de redigir.

## Anexos obrigatorios (context/)
- `context/lei-13966-2019.md` — base material conforme a acusacao: royalties/fundo (art. 2º IX), padrao/suporte (XIII), marca (XIV), nao-concorrencia (XV-b/XXI), COF viciada (art. 2º §2º / art. 4º). **grep do inciso.**
- `context/cpc-faixas-franquia.md` — se a resposta antecede contencioso/execucao (preliminares, arbitragem 337 X, foro 63). **grep + ler a faixa.**

## Objetivo
Produzir a resposta a notificacao recebida que **protege a posicao do cliente**: nega o que e infundado, reconhece e sana o que e devido (purgando a mora quando convem), contrapropoe solucao, **registra ressalvas** e constroi prova/cronologia para a fase judicial — tudo coerente com o lado.

## Quando ativar
- O cliente recebeu uma notificacao extrajudicial e precisa responder no prazo.
- Necessidade de purgar mora, contranotificar ou registrar protesto formal antes de uma acao.

## Metodologia
1. **DEFINIR O LADO (trava side-aware) e ler a notificacao recebida** — extrair: quem notifica, o que exige, o prazo, a clausula/dispositivo invocado, os valores.
2. **Carregar `memoria-de-caso-franquia`** e cruzar cada acusacao com o contrato + COF + `context/`. Checar arbitragem/foro via `competencia-foro-arbitragem-franquia` (se houver clausula compromissoria, a resposta ja sinaliza que a controversia e arbitral — sem renunciar a ela).
3. **Escolher a estrategia (por acusacao):**
   - **Refutar** — o fato e falso/o dispositivo nao se aplica/a culpa e da outra parte (ex.: franqueado alega que reteve royalties porque a franqueadora nao prestou o suporte prometido — *exceptio non adimpleti contractus*).
   - **Reconhecer e purgar** — o debito existe; pagar/sanar no prazo afasta a rescisao/medida (preserva o contrato e a relacao).
   - **Contrapropor** — repactuacao, parcelamento, plano de adequacao ao padrao, distrato amigavel (-> `distrato-amigavel-franquia`).
   - **Ressalvar/protestar** — registrar discordancia, reservar direitos e anunciar contranotificacao/contencioso.
4. **Estrutura da resposta:**
   1. Qualificacao e referencia a notificacao recebida (data, protocolo).
   2. **Resposta ponto a ponto** ao que foi alegado (refuta/reconhece/contrapropoe).
   3. Fundamento — clausula contratual + dispositivo da **Lei 13.966** (e CPC/LPI quando pertinente).
   4. **Providencia adotada** (purga, plano, contraproposta) com prova anexa.
   5. **Ressalvas e reserva de direitos** (e, se for o caso, contranotificacao com exigencia propria — lado franqueado: COF viciada -> art. 2º §2º/art. 4º).
   6. Encerramento de boa-fe (preferencia por solucao extrajudicial) sem abrir mao da defesa judicial.
5. **Atencao ao silencio e a prova:** orientar que ignorar a notificacao pode constituir/agravar a mora e servir de prova contra o cliente; a resposta documenta a versao do cliente. **Nunca confessar alem do necessario.**
6. **Anti-alucinacao:** valores reais do caso; nenhum dispositivo/jurisprudencia sem cruzar o `context/`.

## Cross-check final (obrigatorio)
- `validador-franquia` — dispositivos da Lei 13.966/CPC/LPI conferidos no `context/`; **nenhuma 8.955/94 como vigente**; CDC fora do eixo franqueador x franqueado; arbitragem nao renunciada por descuido.
- `suprema-corte-franchising` (R1-R4) — lado certo? estrategia coerente com a prova? ressalvas preservam a defesa futura? Reprovou -> volta.
