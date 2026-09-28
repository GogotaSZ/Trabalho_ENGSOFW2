# Validação e rastreabilidade

Use este checklist antes da entrega para verificar se o trabalho continua coerente com o projeto preliminar.

## Requisitos funcionais

- [x] RF01: cadastro de motorista/motoboy.
- [x] RF02: cadastro de gerente/coordenador.
- [x] RF03: cadastro de ponto.
- [x] RF04: montagem de roteiro diário.
- [x] RF05: registro de chegada e saída.
- [x] RF06: cálculo de tempo parado.
- [x] RF07: consulta de histórico.
- [x] RF08: gráficos por dia, mês e período.
- [x] RF09: parametrização de custos.
- [x] RF10: parametrização de jornada e regras.
- [x] RF11: cálculo de custo estimado.
- [x] RF12: exportação de relatório.

## Regras de negócio

- [x] RN01: a primeira ocorrência é partida e não gera tempo parado.
- [x] RN02: demais pontos usam saída menos chegada.
- [x] RN03: total do roteiro soma as durações válidas.
- [x] RN04: jornada padrão inicial de 8 horas.
- [x] RN05: roteiro vinculado a um motorista e uma data.
- [x] RN06: pontos com posição sequencial única no roteiro.
- [x] RN07: custo estimado calculado por distância, combustível e rendimento.

## Pontos em aberto

- [ ] Confirmar se custo por km pode ser editado diretamente ou se deve ser sempre derivado.
- [ ] Definir como a distância percorrida será obtida.
- [ ] Confirmar quais regras de cálculo podem ser parametrizadas além da jornada.
- [ ] Confirmar a matriz de permissões por operação.
- [ ] Esclarecer se "entrada de pedidos" será parte do escopo ou apenas referência a endereços.

## Conferência desta etapa

- [ ] Revisar a escrita e a formatação do documento principal.
- [ ] Comparar os diagramas com as descrições dos casos de uso.
- [ ] Verificar se todas as decisões assumidas estão identificadas como decisões de modelagem.
- [ ] Confirmar os pontos em aberto com o professor ou cliente.
- [ ] Preencher os dados acadêmicos da equipe antes da entrega.
- [ ] Gerar as imagens finais dos diagramas para inclusão no documento entregue.
