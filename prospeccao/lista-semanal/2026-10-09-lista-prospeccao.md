# Lista de Prospecção — 09/10/2026

**Região:** Barra da Tijuca e Recreio dos Bandeirantes, RJ
**Segmentos:** imobiliárias e corretores autônomos, padrão médio/alto
**Candidatos encontrados:** 2 imobiliárias · 0 corretores (teto: 50 + 50)

> **Aviso de ambiente, antes da lista:** esta rodada também rodou sem WebFetch funcional — toda
> tentativa de abrir uma página direto (ZAP Imóveis, Instagram, site de imobiliária) voltou
> `ENOTFOUND` na proxy de rede desta sessão. É a mesma limitação já registrada na rodada de
> 02/10/2026. Toda a pesquisa usou só WebSearch (resumos indexados). Isso bloqueou de novo: confirmar
> visualmente atividade recente no Instagram, abrir Google Maps/Perfil da Empresa pra ver nota e
> avaliações, e checar a Biblioteca de Anúncios da Meta. Detalhe completo na seção de Observações.

## Imobiliárias

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|
| 1 | Casas Contemporâneas | casascontemporaneas.com.br | Site próprio indexado, descrição de nicho confirmada por fonte secundária; não foi possível abrir a página pra ver atividade recente | Especialização dedicada — a própria descrição da empresa é "corretora especializada em imóveis contemporâneos de alto padrão, terrenos e lotes, exclusivamente em Barra da Tijuca e Recreio dos Bandeirantes", CRECI-RJ 10931-J |
| 2 | Realler Imóveis | reallerimoveis.com.br | Site próprio indexado; não foi possível abrir a página pra ver atividade recente | Portfólio declarado — site se apresenta como "Imobiliária de Alto Padrão" com curadoria de imóveis em Barra da Tijuca, São Conrado e Zona Sul, CRECI-RJ J 6452 |

## Corretores

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|

*Nenhum corretor autônomo novo passou a barra de sinal nesta rodada — ver "quase entraram" abaixo.*

## Observações

**Por que ficou bem abaixo do teto de 50+50:** mesma causa-raiz da rodada de 02/10/2026 — WebFetch
voltou `ENOTFOUND` em todo domínio testado (ZAP, Instagram, sites próprios de imobiliária, e um
domínio neutro de controle), então o trabalho rodou só com WebSearch. Além disso, esta é a segunda
rodada seguida na mesma região: os candidatos com sinal forte e fácil de confirmar por resumo de
busca (avaliação no Google citada em texto, portfólio grande em agregador, tempo de mercado
declarado em matéria de imprensa) já foram capturados na rodada anterior. Esta rodada teve que ir
mais fundo pra achar nomes novos, e a maior parte do que apareceu não teve sinal de venda e
presença digital confirmáveis ao mesmo tempo — só um dos dois, nunca os dois juntos com confiança.
Recomendação, repetida da rodada passada: rodar com navegador real (Claude in Chrome ou o browser
nativo) eleva bastante o volume e a confiança dos sinais, tanto pra candidatos novos quanto pra
confirmar os que ficaram em "não confirmada" ou "quase entraram" nas duas rodadas.

**Quase entraram, mas faltou sinal ou confiança:**

*Imobiliárias:*
- A+ Boutique Imobiliária (CRECI-RJ 8890-J) — apareceu como anunciante "Premier" num portal, mas uma segunda busca não trouxe nenhum outro sinal (presença própria ou portfólio) pra confirmar.
- Mm Rio Corretora (CRECI-RJ 06388-J) — mesmo caso: só o CRECI apareceu numa busca, nada além disso numa segunda tentativa.
- Sentineli e Sobral — citada como "Imóveis Alto Padrão" num resultado isolado (CRECI 005895-0 no rodapé do site), sem nenhuma corroboração em busca dedicada.
- Elite Imóveis — autodescrição de "imobiliária de alto padrão com atendimento personalizado" (CRECI CJ 5429), mas sem nenhuma fonte independente confirmando atuação ou presença.
- Guimarães Assessoria Imobiliária — especialização declarada em Barra/Recreio/Zona Sul num portal (Wimóveis), mas sem sinal de venda específico (avaliação, portfólio, tempo de mercado).

*Corretores:*
- Italo Lyra — mesmo caso da rodada de 02/10: CRECI-RJ J-34.134, especialista em lançamentos premium citado por um portal, mas sem Instagram ou site próprio localizado nesta rodada também.
- Ronaldo Ivan — citado por uma consultoria (Zona Sul Lançamentos) como corretor com 25+ anos de experiência e atuação em lançamentos premium na Barra, mas o sinal está na página da consultoria, não num canal próprio dele — sem presença digital individual confirmável.
- Best House Consultoria — aparece descrita (numa busca anterior) como especializada em alto padrão em Barra/Recreio, mas uma busca dedicada ao nome não achou site, Instagram nem nenhuma outra fonte independente — ficou sem confirmação nenhuma.

**Checagem de duplicata:** `clientes/` (só duas contas da sogra, fora do setor imobiliário) e
`prospeccao/` (só a pasta `lista-semanal/`, sem pasta de diagnóstico individual ainda aberta) foram
checados — nenhum dos dois candidatos acima é cliente atual ou já foi diagnosticado em pasta
própria. Nenhum dos dois nomes desta rodada também apareceu na lista de 02/10/2026.
