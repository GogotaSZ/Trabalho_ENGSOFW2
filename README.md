# Monitoramento de Tempo Parado em Roteiros

Trabalho acadêmico de Engenharia de Software II dedicado à análise de um sistema para acompanhar roteiros diários, registrar chegadas e saídas e compreender o tempo parado em cada ponto.

Neste momento, o repositório contém somente a documentação da primeira etapa. Não há implementação, banco de dados ou testes de código. A organização acompanha a lógica do nosso próprio projeto: primeiro o entendimento do problema, depois a modelagem e, por fim, a conferência da entrega.

## Organização do trabalho

| Conteúdo | Finalidade |
| --- | --- |
| `documentacao/projeto-preliminar.md` | Documento principal, com escopo, atores, requisitos, casos de uso, regras e classes conceituais. |
| `documentacao/diagramas/` | Fontes dos diagramas apresentados e explicados no projeto preliminar. |
| `documentacao/contexto-operacional.md` | Perfis, auditoria, privacidade e limites do sistema. |
| `documentacao/checklist-de-validacao.md` | Conferência dos requisitos, regras de negócio e pontos ainda abertos. |
| `documentacao/proximas-etapas.md` | Continuidade prevista para o trabalho, sem iniciar a implementação. |

## Ordem de leitura

1. Leia o `projeto-preliminar.md` para conhecer a proposta completa.
2. Consulte os diagramas junto das seções correspondentes do documento principal.
3. Use o `contexto-operacional.md` para revisar responsabilidades e cuidados com os dados.
4. Finalize com o `checklist-de-validacao.md` e registre as decisões pendentes.

## Ideia central

O projeto acompanha um roteiro vinculado a um motorista e a uma data. Os pontos aparecem em ordem; o primeiro representa a partida e não gera tempo parado. A partir do segundo ponto, o tempo é obtido pela diferença entre saída e chegada. O sistema também prevê histórico, gráficos, parâmetros de jornada e estimativa de custo do trajeto.

## Situação atual

A primeira parte está organizada como material de análise e modelagem. Antes de qualquer desenvolvimento, ainda devem ser confirmadas com o professor ou cliente as decisões listadas no documento de próximas etapas.
