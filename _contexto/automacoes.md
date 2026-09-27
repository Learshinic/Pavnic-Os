<!-- quem alimenta: nasce no primeiro registro de rotina ligada; o /atualizar acrescenta quando uma automação é ligada, desligada ou mudada. Lido quando a sessão pede (mapa) e na /faxina. -->
# Automações

> Toda rotina que roda sozinha (cron, worker, agente autônomo) tem uma linha aqui. Rotina que não
> está listada não deveria estar rodando.

## Lista de Prospecção Semanal

- **O que faz:** roda a skill `/prospectar-lista` — gera o relatório semanal de imobiliárias e
  corretores pra prospectar (Barra da Tijuca e Recreio dos Bandeirantes), e um recado avisando.
- **Onde roda:** rotina em nuvem (Claude, cloud routine), sobre o repositório
  `github.com/Learshinic/Pavnic-Os`, branch `main`.
- **Quando:** toda sexta-feira, 18h (horário de São Paulo).
- **Origem que assina:** `agendador` (diário/recados assinados `AAAA-MM-DD-agendador-*`).
- **Como saber se quebrou:** se sexta passar sem um arquivo novo em `prospeccao/lista-semanal/` e
  sem recado novo em `_memoria/recados/`, a rotina não rodou ou falhou. Conferir em
  [claude.ai/code/routines/trig_0158KtFghUucGHywb3MxFox9](https://claude.ai/code/routines/trig_0158KtFghUucGHywb3MxFox9).
- **Criada em:** 26/09/2026.
