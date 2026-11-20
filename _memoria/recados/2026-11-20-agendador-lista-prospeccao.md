de: agendador
quando: 2026-11-20
precisa de ação: sim

Rodei a `/prospectar-lista` semanal (Barra da Tijuca e Recreio dos Bandeirantes, imobiliárias e
corretores autônomos, padrão médio/alto). Resultado: **0 imobiliárias + 0 corretores** entraram na
lista — relatório completo em `prospeccao/lista-semanal/2026-11-20-lista-prospeccao.md`.

**O que precisa da sua decisão:** esta é a **oitava rodada seguida** (desde 02/10) sem WebFetch
funcional nesta sessão. Desta vez testei com domínios de controle fora do nicho (`example.com`,
`google.com`, `instagram.com`) e todos falharam com `ENOTFOUND` — confirma que é bloqueio de rede da
sessão inteira, não uma página específica que resiste à leitura. Sem isso, não dá pra abrir
Instagram, Google Maps/Perfil da Empresa nem a Biblioteca de Anúncios da Meta pra confirmar os
sinais que a skill exige. O volume caiu de 14 candidatos na primeira rodada pra zero ou quase zero
nas últimas cinco rodadas. Esta rodada achou 3 nomes novos com sinal parcial (MySide, Imovelum
Plataforma Imobiliária, Imóvel Aqui) mas nenhum com Instagram/site próprio E sinal de venda
confirmados ao mesmo tempo — detalhe em "quase entraram" no relatório.

Decisão que está em aberto há quase dois meses, agora com mais evidência de que é bloqueio de rede
e não limitação de página: manter a rotina semanal rodando assim (produzindo pouco ou nada), pausar
até o ambiente ter navegador real ou rede liberada pra esses hosts, ou mudar a cadência pra mensal
até resolver o ambiente.
