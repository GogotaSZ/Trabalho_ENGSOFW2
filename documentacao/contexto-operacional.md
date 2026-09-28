# Operação e privacidade

Este documento reúne pontos de apoio para uma futura implementação do sistema. Ele não substitui o projeto preliminar; apenas organiza cuidados operacionais que aparecem nos requisitos não funcionais.

## Perfis

| Perfil | Responsabilidade principal |
| --- | --- |
| Administrador | Mantém cadastros, parâmetros, perfis e acesso amplo aos dados. |
| Gerente/Coordenador | Planeja roteiros, acompanha equipe, consulta histórico e corrige registros autorizados. |
| Motorista/Motoboy | Registra chegada e saída nos pontos do próprio roteiro. |

## Auditoria

Devem gerar registro de alteração:

- edição de endereço ou coordenadas de um ponto;
- correção de horários de chegada ou saída;
- mudanças em parâmetros com impacto em cálculos futuros.

Cada registro deve guardar responsável, instante, tipo de alteração e valores antes/depois.

## Privacidade e LGPD

O sistema trata dados pessoais como nome, telefone, documento, e-mail e histórico operacional. Para uma implementação real, recomenda-se:

- usar controle de acesso por perfil;
- exibir apenas os dados necessários a cada perfil;
- evitar salvar senhas em texto puro;
- registrar acessos e correções relevantes;
- não versionar banco local, senhas, sessões ou arquivos com dados pessoais reais;
- usar dados fictícios em demonstrações acadêmicas.

## Limites atuais

O projeto preliminar não define integração com ERP, mapas, telemetria em tempo real, folha de pagamento ou aplicativo nativo. Qualquer inclusão desse tipo deve ser tratada como expansão de escopo.
