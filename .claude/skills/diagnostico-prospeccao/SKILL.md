---
name: diagnostico-prospeccao
description: >
  Faz um diagnóstico externo, só com fontes públicas, dos canais de aquisição de leads de um
  prospect — imobiliária, corretor ou PME local que ainda não é cliente. Cruza Instagram, a
  Biblioteca de Anúncios da Meta, Google Maps/Perfil da Empresa, TikTok, a Central de
  Transparência de Anúncios do Google e os portais do nicho, e devolve um relatório com tese em
  uma frase, mapa de canais e achados numerados por impacto. É a peça que abre porta antes da
  reunião. Usar sempre que o usuário pedir pra "prospectar", "fazer um diagnóstico de canais de
  aquisição", "analisar o marketing de [nome de negócio]", "ver como [imobiliária/corretor/PME]
  tá indo nas redes/anúncios", ou citar um nome de negócio junto com "abrir porta", "pitch",
  "proposta" ou "reunião marcada com".
---

# /diagnostico-prospeccao

## O que é e quando usar

Este é o diagnóstico que você já validou na prática: o caso da Imoverso Imobiliária gerou uma
reunião real marcada. A lógica se repete pra qualquer alvo — imobiliária, corretor ou PME local.

É pesquisa **sobre um terceiro que ainda não é cliente**, feita só com o que está público. Não é
auditoria de conta própria (isso seria outro processo, pra quando o alvo já é cliente e te dá
acesso à conta de anúncios). Aqui você está de fora olhando pra dentro.

## Antes de começar

Ler `_contexto/empresa.md` e `_contexto/preferencias.md` (mapa do `AGENTS.md`) pra manter o tom na
conversa com o usuário. O relatório em si tem tom próprio (ver "Tom do relatório" abaixo) — ele não
segue o guia de marca, porque não é peça que fala com o cliente final, é prova de competência pro
prospect ver.

## Passo 1 — Receber o alvo

Perguntar (ou confirmar, se já veio na mensagem):
- Nome do negócio e cidade/bairro
- Nicho (imobiliário, ou qual outro)
- Links que já existirem: Instagram, site, Facebook

O que faltar, ir buscar com WebSearch antes de partir pra navegação — não travar a entrevista
pedindo tudo de uma vez.

## Passo 2 — Coletar por canal

Usar as ferramentas do navegador (`mcp__Claude_Browser__*`: `navigate`, `computer`, `get_page_text`,
`read_page`) pra cada canal abaixo — a maioria dessas páginas carrega via JavaScript, então
`WebFetch` sozinho não basta. `WebSearch`/`WebFetch` nativos servem de apoio pra achar o link certo
quando faltar.

**Instagram orgânico** — seguidores, quantidade de posts, bio, frequência de reels/posts recentes,
o que performa acima da média (ex: um reel com views muito acima da mediana dos últimos 10-12).

**Biblioteca de Anúncios da Meta** (`facebook.com/ads/library`, país BR, buscar pelo nome da
página) — quantos anúncios ativos, desde quando cada um roda, formato (imagem/vídeo/carrossel),
CTA e destino (formulário instantâneo vs site), ângulo de copy, quantas variações do mesmo
produto/oferta rodando ao mesmo tempo, sinais de "baixo volume de impressões".

**Google Maps / Perfil da Empresa no Google** — nota, quantidade de avaliações, endereço,
telefone. Comparar esse telefone com os telefones que aparecem nos outros canais (site, Linktree,
WhatsApp do anúncio) — divergência de contato é um achado clássico e vale ouro.

**TikTok** — seguidores, curtidas, views médias dos últimos vídeos.

**Central de Transparência de Anúncios do Google** (`adstransparency.google.com`) — roda Google
Ads pro domínio do prospect ou não.

**Portais do nicho** — pra imobiliário, ZAP/Viva Real; pra outros nichos, adaptar (ex: iFood pra
restaurante, Google Shopping pra e-commerce). Se não achar página do anunciante, registrar como
"não confirmado", nunca inventar número.

**Site do prospect** — tem pixel Meta, GA4 ou Google Tag Manager no HTML? Os números de
WhatsApp/telefone batem entre o site e os outros canais? Os links de redes sociais no site apontam
pro lugar certo (ou levam pra outra empresa por engano)?

Anotar a data da coleta em cada fonte — o relatório final cita isso.

## Passo 3 — Cruzar num mapa de canais

Montar uma tabela: **Canal · Papel no funil · Alcance/tamanho · Status · Leitura**. Status é
qualitativo: Forte · Em construção · Frágil · Crítico · Ausente/Não confirmado.

## Passo 4 — Resumo executivo

Uma **tese** em uma frase (o diagnóstico central, não uma lista — algo como "boa oferta e bom
criativo, mas o funil vaza entre o clique e o atendimento"), seguida de uma tabela de
**números-chave** (indicador · valor) com os 8-12 fatos mais fortes que você coletou.

## Passo 5 — Achados principais

Listar de 3 a 5, numerados por impacto (o mais grave primeiro). Cada um precisa de **evidência
concreta** coletada no passo 2 — nunca uma opinião solta. Formato: "**Nome curto do problema.**
Evidência específica (números, prints mentais do que foi visto). *Por que isso importa.*"

## Passo 6 — Onde o aproveitamento se perde

Tabela: **# · Problema · Evidência · Impacto**. É a seção mais densa — pode ter 5-9 linhas, cada
uma um ponto isolado (fragmentação de verba, falta de pixel, mensagem conflitante, etc).

## Passo 7 — Nota de método

Fechar com: fontes usadas, data da coleta, e uma frase deixando claro o que **não** dá pra saber
de fora (investimento real, custo por lead, volume de leads — isso nunca é público, não fingir que
é).

## Formato do arquivo final

Salvar em `prospeccao/<slug-do-alvo>/diagnostico-canais-<slug-do-alvo>.md`, seguindo esta estrutura
(o mesmo formato do caso Imoverso):

```markdown
# [Nome do Prospect] — Diagnóstico de Canais de Aquisição de Leads

**Empresa:** [nome] · [cidade/bairro]
**Data da coleta:** [DD/MM/AAAA]
**Fontes:** [lista dos canais checados]
**Método:** análise externa (outside-in). Tudo coletado de fontes públicas. Investimento, custo
por lead e volume de leads não aparecem publicamente.

## 0. Resumo executivo

**Tese:** [uma frase]

### Números-chave

| Indicador | Valor |
|---|---|
| ... | ... |

### Os achados principais

1. **[nome curto].** [evidência]. *[impacto]*
2. ...

## 1. Mapa de canais

| Canal | Papel no funil | Alcance/tamanho | Status | Leitura |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

## 2. Mídia paga

[o que está bom / onde o aproveitamento se perde, com a tabela de achados numerados]

## 3. Orgânico (Instagram, TikTok, Facebook)

[perfil, frequência, o que performa]

## 4. Site e mensuração

[pixel/GA4/GTM, divergência de contato, links quebrados]

## 5. Nota de método
[fontes, data, limites do que dá pra saber de fora]
```

## Depois de gerar

Perguntar se quer que o relatório seja convertido pra Google Docs (o conector Google Drive/Docs já
está ligado nesta conta) — deixa pronto pra enviar ou levar pra uma reunião.

## Tom do relatório

Analítico e direto: tese em uma frase, achados numerados com evidência, tabelas. Isso é prova de
competência pro prospect ver, não uma peça de marca — não usa o guia de `_contexto/marca/` aqui.
A conversa **com o usuário** (perguntas, confirmações) sim segue `_contexto/preferencias.md`:
natural, sem clichês de IA.

## Regras

- Nunca inventar número ou dado que não foi coletado. "Não confirmado" é resposta válida.
- Evidência concreta em cada achado — se não tem evidência, não é achado, é palpite.
- Uma reunião marcada é o critério de sucesso desse processo — se o alvo já demonstrou interesse
  ou já é conhecido, adaptar o tom pra reforçar o que já está andando, não repetir do zero.
