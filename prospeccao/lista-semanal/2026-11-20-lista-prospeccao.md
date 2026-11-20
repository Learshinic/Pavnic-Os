# Lista de Prospecção — 20/11/2026

**Região:** Barra da Tijuca e Recreio dos Bandeirantes, RJ
**Segmentos:** imobiliárias e corretores autônomos, padrão médio/alto
**Candidatos encontrados:** 0 imobiliárias · 0 corretores (teto: 50 + 50)

> **Aviso de ambiente, antes da lista:** oitava rodada seguida sem WebFetch funcional. Testei de
> novo nesta rodada, com três domínios de controle (`example.com`, `www.google.com`,
> `www.instagram.com`) e todos voltaram `ENOTFOUND` na proxy de rede desta sessão — mesmo bloqueio
> das rodadas de 02/10, 09/10, 16/10, 23/10, 30/10, 06/11 e 13/11. Isso confirma que não é um
> problema de página específica (JS-pesada, bloqueio de bot): é a sessão inteira sem rota de rede
> pra qualquer host fora da lista permitida, incluindo `google.com`. Toda a pesquisa desta rodada
> rodou só com WebSearch (resumos indexados), nunca com leitura direta de página, Instagram, Google
> Maps/Perfil da Empresa ou Biblioteca de Anúncios da Meta. Detalhe completo na seção de
> Observações.

## Imobiliárias

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|

*Nenhuma imobiliária nova passou a barra de sinal nesta rodada — ver "quase entraram" abaixo.*

## Corretores

| # | Nome | Instagram/site | Sinal de presença digital | Sinal de venda (proxy) |
|---|---|---|---|---|

*Nenhum corretor autônomo novo passou a barra de sinal nesta rodada — ver "quase entraram" abaixo.*

## Observações

**Por que ficou zerado:** mesma causa-raiz das sete rodadas anteriores — sem WebFetch, não dá pra
abrir Instagram, Google Maps/Perfil da Empresa ou a Biblioteca de Anúncios da Meta pra confirmar
atividade recente (postou nas últimas 2 semanas), avaliação ou posts de venda. Esta é a oitava
rodada seguida na mesma região: 14 imobiliárias + 4 corretores entraram no total desde 02/10, e
zero entrou nas três últimas rodadas (23/10 em diante, com exceção de 1 em 30/10). Esta rodada
testou ângulos de busca ainda não tentados nas sete anteriores (post de Instagram com "vendido" ou
"chaves entregues" citado em texto indexado, imobiliária "boutique" especializada em lançamentos de
alto padrão, prêmios/premiações do setor em 2026, perfis específicos de corretores citados em
diretórios como Apto.vc, ranking Heepsy de influenciadores de Instagram do setor imobiliário,
associados do Secovi Rio) e achou nomes novos (ver abaixo), mas nenhum teve ao mesmo tempo presença
digital própria confirmada (Instagram ou site da própria empresa, não perfil de portal/diretório
como ZAP/VivaReal/Apto.vc/MGF Imóveis) **e** sinal de venda confiável em padrão médio/alto
confirmado de forma independente — a combinação que a skill exige pra entrar na lista.

**Recomendação, repetida (e reforçada) das sete rodadas passadas:** esta automação já roda há oito
semanas sem navegador real, e o teste desta rodada deixa isso mais claro ainda — não é limitação de
página específica, é bloqueio de rede da sessão pra qualquer host fora da lista permitida
(`google.com` também falhou). O volume foi de 14 candidatos (02/10) pra zero ou quase zero nas
últimas cinco rodadas. Rodar com navegador real (Claude in Chrome ou o browser nativo) ou liberar
os hosts necessários (Instagram, Google Maps/Perfil da Empresa, Biblioteca de Anúncios da Meta) na
configuração de rede da sessão eleva bastante o volume e a confiança dos sinais — principalmente
pra achar corretores autônomos, que praticamente só aparecem via Instagram/hashtag, não via busca
textual indexada. Continua valendo uma decisão sua: manter a rotina semanal do jeito que está
(produzindo pouco ou nada, rodada após rodada, há quase dois meses), pausar até o ambiente ter
navegador real/rede liberada, ou mudar a cadência pra mensal até resolver o ambiente.

**Quase entraram, mas faltou sinal ou confiança (nomes novos desta rodada, não repete nomes já
avaliados nas rodadas de 02/10 a 13/11, entrados ou descartados):**

*Imobiliárias:*
- MySide (myside.com.br) — plataforma de "personal shopper imobiliário" especializada em imóveis
  novos/na planta, com portfólio ativo quase inteiramente em Barra da Tijuca (nomes de
  empreendimentos citam a região diretamente: We Barra by Living, Sensia Barra, Signature Praia do
  Pepê, Duet Barra, Endless Península, entre outros de VGV alto — grifes como Artefacto e Breton
  associadas a alguns lançamentos do bairro). Site próprio confirmado por múltiplas páginas
  indexadas (contato, "sobre nós", blog institucional). Não entrou porque: (1) nenhuma busca
  dedicada confirmou Instagram próprio nem WebFetch pra abrir um e confirmar atividade recente; (2)
  o portfólio é majoritariamente pré-venda/lançamento (corretora de novos empreendimentos), o que é
  sinal de presença forte mas não necessariamente de "venda consistente" fechada no sentido que a
  skill pede — fica como sinal parcial, não combinação completa.
- Imovelum Plataforma Imobiliária (CRECI 8951-J-RJ; 43 imóveis cadastrados em Barra da Tijuca, 178
  no Rio; lançamento mais recente citado, Barra Home Design, de jun/2026) — presença institucional e
  CRECI confirmados num diretório (Apto.vc), mas nenhuma busca dedicada achou Instagram ou site
  próprio independente do diretório.
- Imóvel Aqui (CRECI 8159-J-RJ; cerca de 25 imóveis cadastrados em Barra da Tijuca; lançamento mais
  recente citado, Riio by Piero Lissoni, de jun/2026) — mesma situação: presença e CRECI confirmados
  só em diretório (Apto.vc), sem Instagram ou site próprio confirmado por busca dedicada.

*Corretores:* nenhum nome novo chegou perto de confirmar presença digital própria nesta rodada —
buscas por corretores específicos citados em diretórios (ex.: Raphael Brandão Baptista da Silva,
especializado em lançamentos do Recreio segundo a Apto.vc) só devolveram o próprio perfil de
diretório, sem Instagram ou site pessoal achável por busca textual. A busca por
corretores-influenciadores do setor imobiliário (ranking Heepsy) não trouxe nenhum nome ligado à
Barra da Tijuca ou ao Recreio — os exemplos encontrados atuam em São Paulo ou fora do Brasil.

**Ainda em aberto, sem reavaliação nesta rodada (carregado de 13/11, nenhuma informação nova
buscada):** Matchimob, Infinity Corretora de Imóveis e Gilberto Almeida Imóveis continuam sem
Instagram/site próprio confirmado, e Ativa Imobiliária, Horizon Rio, MN Imóveis, Luciana Ferreira
Imóveis e as unidades Lopes Enjoy (RB/FN) seguem no mesmo estado reportado em 13/11 (ver aquele
relatório para o detalhe de cada um).

**Checagem de duplicata:** `clientes/` (vazia além do `.gitkeep` — nenhuma imobiliária/corretor
cliente hoje) e `prospeccao/` (só contém a própria pasta `lista-semanal/`, sem pastas de diagnóstico
individual abertas) foram checados. Nenhum nome desta rodada (incluindo os da seção "quase
entraram") é cliente atual nem já foi diagnosticado em pasta própria. Nomes já avaliados em rodadas
anteriores (entrados: Patrimóvel, Special Residence, EGiovanelli, Privilégio Imóveis, Grupo
JTavares, Francisco Campos, RE/MAX Ocean Eagle, RE/MAX Riserva, Ciganimóveis, Prime Rio Imóveis,
Casas Contemporâneas, Realler Imóveis, Andreata Gestão Imobiliária, Américas Imóveis, Luiz Carlos,
Gisely Marques, Ronaldo Carreiro, José Luiz Leão; descartados ou "quase entraram" sem confirmação:
Martins Ferreira Imóveis, Marcia Ewerton, IMOPAR, Coelho da Fonseca, Brasil Brokers, A+ Boutique, Mm
Rio Corretora, Sentineli e Sobral, Elite Imóveis, Guimarães Assessoria, INC. Imobiliária 01 e 02,
Fórmula Imobiliária, ATMA Imóveis, IMOBELLO, Casa ParKes, Alicson Machado, Imobiliária Alto Padrão na
Barra da Tijuca, RioImob, ABN Corretora de Imóveis, Sol Menezes Imóveis, Sawala Consultoria
Imobiliária, Muller Imóveis RJ, Block Imóveis Recreio, Recreio Imóveis, Barra Olímpica Imobiliária,
REMAX Sky/Vix, Confiart/Confiar Imóveis, Imobiliária Bandeirantes, Podium Imobiliária, Morar Rio,
Martinelli Imóveis, JB Andrade, Julio Bogoricin, Thales Castro, Paulo A. Cruz, Italo Lyra, Fernanda
Freitas, Ronaldo Ivan, Best House Consultoria, Rafael Calixto de Moraes, Rosane Nunes, Jhéssica
Soares, Mauro Maidantchik, Isabelle Simonard Rodrigues dos Santos, Ronaldo Batista da Fonseca,
Caroline Rodrigues Gonçalves, Mahnai Imobiliária e Turismo, Ativa Imobiliária, Horizon Rio, MN
Imóveis, Luciana Ferreira Imóveis, Lopes Enjoy Imóveis RB/FN, Matchimob, Infinity Corretora de
Imóveis, Gilberto Almeida Imóveis) não foram reincluídos nesta rodada. A Imoverso Imobiliária (caso
de referência de diagnóstico, set/2026, registrado em `_contexto/empresa.md`) também não apareceu
nesta rodada e continua fora da lista por já ter sido trabalhada.
