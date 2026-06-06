# Sistema de Gestão para Ginásios

## 1. Capa

Sistema de Gestão para Ginásios  
Desktop + API Web + Sincronização Centralizada

## 2. Visão geral

O sistema centraliza a operação do ginásio: utentes, contratos, pagamentos,
acessos, caixa, loja, colaboradores, acompanhamento físico, CRM e comunicação
por SMS.

## 3. Objetivo do sistema

- Reduzir controlo manual.
- Evitar entradas indevidas.
- Melhorar gestão financeira.
- Acompanhar evolução dos utentes.
- Fidelizar clientes com CRM, bónus e SMS.
- Preparar o grupo para várias unidades sincronizadas.

## 4. Módulos principais

- Usuários, perfis e permissões.
- Utentes e contratos.
- Pacotes e subscrições.
- Acessos por cartão/tag.
- Avaliações físicas e evolução.
- Produtos, serviços e vendas.
- Caixa e transações financeiras.
- CRM, bónus, campanhas e SMS.
- Sincronização com API web.

## 5. Usuários e permissões

O sistema permite criar perfis como Gestor, Treinador, Recepcionista, Caixa e
Administrador. Cada perfil recebe uma lista de permissões, garantindo que cada
colaborador acesse apenas as funcionalidades autorizadas.

## 6. Gestão de utentes

- Cadastro completo do utente.
- Foto e dados de contacto.
- Estado do utente.
- Histórico de contratos.
- Histórico de pagamentos.
- Histórico de acessos.
- Acompanhamento físico.
- Fidelização e bónus.

## 7. Pacotes, subscrições e contratos

O ginásio pode criar pacotes diários, semanais, quinzenais, mensais, anuais ou
avulsos. Cada utente fica ligado a um contrato, com datas de início e fim,
estado, preço, renovações e possíveis taxas de reativação.

## 8. Controlo de acessos

Os utentes e colaboradores podem entrar com cartão, tag ou outro dispositivo. O
sistema valida contrato, pagamento, dispositivo e regras de acesso antes de
autorizar a entrada na catraca.

## 9. Avaliação física e evolução

O sistema agenda e regista avaliações periódicas do utente, permitindo controlar
peso, medidas, objetivos, observações do treinador e próxima data de avaliação.

## 10. Loja, produtos e serviços

O ginásio pode vender suplementos, água, equipamentos, aulas extras, serviços de
personal trainer e outros serviços. O sistema controla cadastro, preço, estoque,
vendas e movimentos de produtos/serviços.

## 11. Caixa e transações

O caixa regista entradas e saídas financeiras de diferentes origens:

- Pagamentos de mensalidade, anuidade ou planos avulsos.
- Venda de produtos.
- Venda de serviços.
- Reativação de contratos.
- Ajustes, devoluções e outras movimentações.

## 12. CRM, bónus e SMS

O CRM ajuda a manter o utente ativo e fidelizado:

- Mensagens de boas-vindas.
- Avisos de vencimento.
- SMS para utentes ausentes.
- Lembretes de avaliação física.
- Campanhas promocionais.
- Bónus por fidelização.
- Mensagens de aniversário.
- Recuperacao de clientes inativos.

## 13. Critérios para SMS

Exemplos de critérios configuraveis:

- Enviar SMS X dias antes do vencimento do contrato.
- Enviar SMS quando o contrato vencer.
- Enviar SMS se o utente faltar por 7, 15 ou 30 dias.
- Enviar SMS no aniversário.
- Enviar SMS quando houver bónus disponível.
- Enviar SMS para campanhas ou reativação.

## 14. Várias unidades do mesmo grupo

Utentes podem frequentar outras unidades do mesmo grupo, respeitando regras
configuraveis. Se os pacotes/preços forem diferentes, o sistema pode limitar o
acesso a uma quantidade configurada de dias, por exemplo 10 dias.

## 15. Desktop, offline e API web

O app desktop será desenvolvido em C# WPF com arquitetura limpa. Ele poderá
operar localmente e sincronizar dados com uma API web centralizada quando houver
internet, mantendo a operação do ginásio mesmo em cenários offline.

## 16. Arquitetura proposta

- Domínio: regras centrais do negócio.
- Aplicação: casos de uso.
- Infraestrutura: banco de dados, API, catraca, SMS e integrações.
- WPF/UI: telas desktop.
- API Web: dados centralizados, sincronização e expansão futura.

## 17. Benefícios para o cliente

- Maior controlo operacional.
- Menos perdas financeiras.
- Melhor experiência para o utente.
- Decisões baseadas em dados.
- Mais fidelização.
- Preparação para crescimento em grupo.
- Automatização de acessos, comunicação e pagamentos.

## 18. Fecho

O sistema será uma plataforma completa para gerir o ginásio de ponta a ponta,
desde a entrada do utente até ao pagamento, acompanhamento, comunicação,
fidelização e gestão multiunidade.


## 19. Roadmap por etapas

Etapa 1: sistema desktop base, sem CRM, sem Web API, sem mobile e sem
integração com outros ginásios. Inclui backup na nuvem.

Etapa 2: Web API, painel web para monitoramento remoto, sincronização, CRM,
campanhas, bónus e SMS.

Etapa 3: app mobile para utentes, com histórico, pagamentos, desempenho,
contrato atual, bónus e notificações.

## 20. Estimativa considerando base existente

Como já existe uma base forte em arquitetura limpa e UI WPF, a estimativa
considera adaptação do sistema atual ao domínio do ginásio:

- Etapa 1: 25 a 40 dias de trabalho.
- Etapa 2: 25 a 40 dias de trabalho.
- Etapa 3: 20 a 30 dias de trabalho.
- Total: 70 a 110 dias de trabalho.

As estimativas consideram uma rotina de 9 horas por dia e 5 dias por semana.
