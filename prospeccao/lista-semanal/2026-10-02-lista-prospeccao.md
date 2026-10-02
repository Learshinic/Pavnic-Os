# Lista de Prospecção — 02/10/2026

**Região:** Barra da Tijuca e Recreio dos Bandeirantes, RJ
**Segmentos:** imobiliárias e corretores autônomos, padrão médio/alto
**Candidatos encontrados:** 10 imobiliárias · 4 corretores (teto: 50 + 50)

> **Aviso de ambiente, antes da lista:** esta rodada rodou sem WebFetch funcional — a proxy de rede
> desta sessão bloqueou (`EGRESS_BLOCKED`) todo domínio testado (ZAP Imóveis, Viva Real, Wimoveis,
> Instagram, sites próprios de imobiliárias, e até um domínio neutro de controle). Toda a pesquisa
> usou só WebSearch (resumos indexados), sem abrir nenhuma página diretamente. Isso bloqueou duas
> coisas que a skill pede: confirmar visualmente atividade recente no Instagram (data do último
> post) e checar Google Maps / Biblioteca de Anúncios da Meta (exigem JS). Por isso o volume ficou
> bem abaixo do teto — não por escassez real da região, que claramente sustenta mais candidatos.
> Detalhe completo na seção de Observações.

## Imobiliárias

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|
| 1 | Patrimóvel | patrimovel.imb.br / patrimovel.com.br | Site próprio confirmado por fonte secundária; não foi possível abrir a página pra confirmar atividade recente | Portfólio ativo — 15 imóveis listados na Barra da Tijuca no agregador Apto (além de Ipanema/Copacabana/Botafogo), lançamento recente "Soul Rio – Home Collection" (11/2025), CRECI-RJ 9272-J |
| 2 | Special Residence (imóveis) | Não localizado (handle/domínio não apareceu nas buscas) | **Não confirmada** — incluída apesar disso por sinal de venda forte; checar manualmente antes de prospectar | 35 anos de mercado, 17 anos específicos na Barra da Tijuca, 100% de avaliações positivas no Google, especialização por rua/condomínio de padrão alto (Av. Lúcio Costa, ABM/Bosque Marapendi, Mandalla, Novo Leblon) |
| 3 | EGiovanelli Negócios Imobiliários | Não confirmado (fonte cita "presença ativa em redes sociais", sem handle) | **Não confirmada** | 10+ anos de atuação em Barra/Recreio/Zona Sul, setor PRIME dedicado a alto padrão (mansões, coberturas) |
| 4 | Privilégio Imóveis | Não confirmado | **Não confirmada** | Maior imobiliária do Rio (11 lojas, 20.000+ imóveis na base), aquisição recente da Sawala (expansão zona oeste), atuação no segmento de luxo na Barra |
| 5 | Grupo JTavares | Não confirmado | **Não confirmada** | Fundada em 1994, 30+ anos, especializada em lançamentos de luxo, escritórios em Ipanema e Barra da Tijuca |
| 6 | Francisco Campos Imóveis | Não confirmado | **Não confirmada** | Avaliação média 5,00 no Google com 127+ avaliações, sede na Barra da Tijuca |
| 7 | RE/MAX Ocean Eagle (Barra da Tijuca) | Não confirmado (franquia costuma ter perfil próprio, handle não localizado) | **Não confirmada** | Avaliação 5,00 no Google, elogios específicos a atendimento e portfólio |
| 8 | RE/MAX Riserva (Barra da Tijuca) | Não confirmado | **Não confirmada** | Descrita como referência de mercado na região, opera junto ao empreendimento Riserva Golf (padrão alto) |
| 9 | Ciganimóveis (Barra da Tijuca) | Não confirmado | **Não confirmada** | Avaliação 5,00 no Google com 42 avaliações, atendimento especializado |
| 10 | Prime Rio Imóveis | Não confirmado | **Não confirmada** | Portfólio — 13 imóveis ativos na Barra da Tijuca somados a Ipanema/Leblon/Botafogo/Copacabana no agregador Apto, CRECI-RJ 11994-J |

## Corretores

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|
| 1 | Luiz Carlos | instagram.com/luiz_rodrigues08 | Perfil ativo e indexado; data do último post não confirmável (Instagram fora de alcance) | Tempo de atuação — bio cita 19 anos de experiência, especialização em imóveis de luxo na região |
| 2 | Gisely Marques | instagram.com/giselymarques_ | Perfil ativo, ~12 mil seguidores; data do último post não confirmável | Prova social / portfólio — bio declara atendimento a mais de 440 famílias na Barra da Tijuca; CRECI-RJ 90588 / CRECI PJ 13026 |
| 3 | Ronaldo Carreiro | instagram.com/ronaldocarreirobroker | Perfil ativo, ~23 mil seguidores; data do último post não confirmável | Portfólio/vendas declaradas — bio cita +500 imóveis vendidos e 15 anos de atuação no Rio/Barra da Tijuca |
| 4 | José Luiz Leão ("Imóveis Barra") | joseluizleao.wordpress.com (sem Instagram pessoal localizado) | Site/blog próprio confirmado; sem rede social encontrada — presença mais fraca que os demais no critério de atividade recente | Portfólio em padrão alto — descrito por fonte terceira como tendo vendido 200+ imóveis em empreendimentos de luxo nomeados (Cyano Exclusive Residences, Península, Ilha Pura), ~30 anos de mercado |

## Observações

**Por que ficou bem abaixo do teto de 50+50:** esta rodada rodou sem navegador real — WebFetch
voltou erro `EGRESS_BLOCKED` em todo domínio testado nesta sessão (portais, Instagram, sites
próprios, e até um domínio neutro usado como controle). Isso impediu: confirmar handle de Instagram
pra boa parte das imobiliárias (os resumos de busca raramente citam o link direto), confirmar data
de post pra qualquer candidato, e checar Google Maps/Biblioteca de Anúncios da Meta (exigem
renderização JS). O trabalho rodou só com WebSearch — resumos indexados, nunca leitura direta de
página. O número final reflete essa limitação de ferramenta, não escassez real da região: Barra da
Tijuca e Recreio sustentam claramente um mercado maior do que isso. Recomendação pra próxima rodada:
rodar com acesso a navegador real (Claude in Chrome ou o browser nativo) pra elevar bastante o
volume e confirmar presença digital com os próprios olhos.

**Linhas marcadas "não confirmada":** o sinal de venda é real (citado por fonte com URL), mas a
presença digital não foi vista diretamente — só afirmada por uma fonte secundária ou ausente nas
buscas. Checar manualmente (Instagram, site, Google Meu Negócio) antes de prospectar essas linhas.

**Quase entraram, mas faltou sinal ou confiança:**

*Imobiliárias:*
- Martins Ferreira Imóveis (Recreio, desde 2001) — tempo de atuação, mas sem avaliação, portfólio de padrão alto ou digital confirmado.
- Marcia Ewerton Imóveis (Barra da Tijuca, desde 2011) — tempo de atuação curto, nenhum outro sinal.
- IMOPAR (Barra da Tijuca) — aparece em diretório, sem avaliação nem outro sinal de venda.
- Coelho da Fonseca — tradição e foco em alto padrão confirmados, mas é marca historicamente ligada a São Paulo; não achamos evidência de atuação direta e recorrente em Barra/Recreio especificamente.
- Brasil Brokers — tem presença na Barra da Tijuca, mas é portal/holding de corretoras, não imobiliária única com perfil próprio.

*Corretores:*
- Thales Castro (@thalescastroimoveis) — presença confirmada (8.858 seguidores, atua na Barra/Zona Sul), mas nenhum sinal de venda específico encontrado.
- Paulo A. Cruz (@thebrokerbrasiloficial) — presença confirmada, mas dados conflitantes entre buscas (seguidores, foco de mercado) — baixa confiabilidade da fonte, não incluído.
- Italo Lyra — sinal de venda/tempo forte (CRECI-RJ J-34.134, 12-20+ anos, especialista em Recreio dos Bandeirantes), mas sem Instagram/site localizado — ficou de fora só pela falta de link verificável de presença digital.
- Fernanda Freitas (@imoveisfernandafreitas) — presença confirmada, mas região de atuação e sinal de venda não confirmados para Barra/Recreio especificamente.

**Descartados por serem imobiliária, não corretor autônomo (não contam como "quase entraram"):**
Muller Imóveis RJ, Block Imóveis Recreio, Recreio Imóveis, Realler Imóveis, Barra Olímpica
Imobiliária, REMAX Sky/Vix Barra da Tijuca, Confiart Imóveis, Imobiliária Bandeirantes, Podium
Imobiliária, Morar Rio, Martinelli Imóveis, JB Andrade, Julio Bogoricin.

**Descartados por serem de outra região (falso-positivo de nome):** Diego Wantowsky e Bruno Cassola
(atuam em Balneário Camboriú/SC), Jonatas Rodrigues (CRECI-MG).

**Checagem de duplicata:** `clientes/` e `prospeccao/` estavam sem entradas anteriores no momento
desta rodada — nenhum candidato acima é cliente atual ou já foi diagnosticado em pasta própria.
Vale lembrar, por fora dessa checagem automática: a Imoverso Imobiliária (Barra da Tijuca) já foi
usada como caso de referência de diagnóstico em set/2026 (registrado em `_contexto/empresa.md`) —
não apareceu nesta lista, mas se aparecer em rodadas futuras, não deve reentrar.
