---
name: prospectar-lista
description: >
  Varre uma região em busca de imobiliárias e corretores autônomos com presença digital ativa e
  sinais (proxy, não confirmados) de venda consistente em padrão médio/alto, e devolve uma lista
  ranqueada de candidatos pra prospectar na semana seguinte. É o funil de entrada do
  `/diagnostico-prospeccao`: gera a lista, o diagnóstico mergulha fundo em UM nome escolhido dela.
  Roda automaticamente toda sexta-feira às 18h (rotina agendada), mas também pode ser chamada à
  mão. Usar quando o usuário pedir "lista de prospecção", "quem prospectar essa semana",
  "levantar imobiliárias/corretores pra prospectar", ou mencionar volume ("50 imobiliárias",
  "lista semanal de leads").
---

# /prospectar-lista

## O que é e o que NÃO é

Gera uma lista qualificada de candidatos a prospect — não faz o mergulho fundo em cada um (isso é
o `/diagnostico-prospeccao`, rodado depois, à mão, em 1 nome de cada vez). Esta skill é sourcing e
triagem em volume; a outra é diagnóstico em profundidade.

**Sinal, não confirmação.** Volume de vendas real (quantas vendas por mês) não é informação
pública. Tudo que esta skill reporta sobre "consistência de venda" é **proxy** — evidência indireta
— e precisa ser rotulado como tal no relatório. Nunca apresentar um proxy como se fosse número
confirmado.

## Escopo (padrão, ajustável por pedido)

- **Região:** Barra da Tijuca e Recreio dos Bandeirantes, RJ (primeira rodada; expandir quando o
  usuário pedir outra região)
- **Segmentos:** imobiliárias e corretores autônomos
- **Padrão:** imóveis médio/alto padrão
- **Meta por rodada:** até 50 imobiliárias + 50 corretores — **é teto, não meta obrigatória.** Se a
  região não sustentar esse volume com sinal real de qualidade, reportar o número real encontrado e
  dizer por quê ficou abaixo. Nunca completar a lista com nome fraco só pra bater 50.

## Passo 1 — Levantar candidatos

Usar WebSearch, Google Maps e os portais do nicho (ZAP, Viva Real) pra listar imobiliárias e
corretores atuantes na região. Fontes úteis: busca "imobiliária Barra da Tijuca", "corretor de
imóveis Recreio", páginas de anunciante nos portais, perfis de Instagram que aparecem em buscas de
hashtag/localização da região.

## Passo 2 — Checar sinais de presença digital ativa

Pra cada candidato: tem Instagram com atividade recente (postou nas últimas 2 semanas)? Tem site?
Aparece na Biblioteca de Anúncios da Meta (mesmo que só espiar rapidamente, sem o mergulho completo
do diagnóstico)? Isso é rápido — não é o passo a passo completo do `/diagnostico-prospeccao`, é uma
checagem leve de "existe e está ativo".

## Passo 3 — Checar sinais (proxy) de venda consistente em padrão médio/alto

Sinais válidos, sempre citando qual foi usado:
- Posts recorrentes de "vendido"/"contrato fechado"/"chaves entregues"
- Portfólio ativo com imóveis na faixa de preço médio/alto (não entrada/popular)
- Tempo de atuação (perfil antigo, histórico de posts consistente)
- Prova social (depoimentos, avaliações no Google com menção a compra/venda)

Se não achar nenhum sinal desses pro candidato, ele não entra na lista — presença digital sozinha,
sem sinal de venda, não qualifica.

## Passo 4 — Excluir duplicata

Antes de finalizar, checar `clientes/` (já é cliente) e as pastas já existentes em `prospeccao/`
(já foi diagnosticado antes) — não incluir quem já está em uma dessas duas.

## Passo 5 — Gerar o relatório

Salvar em `prospeccao/lista-semanal/AAAA-MM-DD-lista-prospeccao.md`:

```markdown
# Lista de Prospecção — [DD/MM/AAAA]

**Região:** Barra da Tijuca e Recreio dos Bandeirantes, RJ
**Segmentos:** imobiliárias e corretores autônomos, padrão médio/alto
**Candidatos encontrados:** [N] imobiliárias · [N] corretores (teto: 50 + 50)

## Imobiliárias

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|
| 1 | ... | ... | ... | ... |

## Corretores

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|
| 1 | ... | ... | ... | ... |

## Observações

[se ficou abaixo do teto de 50+50, explicar por quê; candidatos que quase entraram mas faltou
sinal; qualquer coisa que vale contexto pra quem for escolher o próximo alvo]
```

## Passo 6 — Se estiver rodando como rotina agendada (sem ninguém na frente)

Seguir o contrato do robô (`AGENTS.md`, seção 6): criar o relatório novo direto na pasta (passo 5
acima), e deixar um recado em `_memoria/recados/AAAA-MM-DD-agendador-lista-prospeccao.md`:
`de: agendador` · `quando:` · `precisa de ação: sim` · resumo de quantos candidatos entraram e o
caminho do relatório. **Não** promover isso pra `_contexto/agora.md` sozinho — quem lê o recado e
decide levar pra `agora.md` (via `/atualizar`, ou o próprio usuário na próxima sessão) é humano.

## Depois de gerar (quando rodando com o usuário na frente)

Perguntar qual nome do topo da lista ele quer levar pro `/diagnostico-prospeccao` primeiro.

## Regras

- Nunca inventar candidato pra bater o número 50+50. Quantidade real > quantidade redonda.
- Todo sinal de venda é proxy — rotular sempre, nunca apresentar como confirmado.
- Não duplicar quem já é cliente ou já foi diagnosticado.
- Rodando sozinha (agendada): só cria arquivo novo e recado; nunca edita `_contexto/` ou
  `_memoria/decisoes.md`.
