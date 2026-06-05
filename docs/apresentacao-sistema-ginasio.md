# Sistema de Gestao para Ginasios

## 1. Capa

Sistema de Gestao para Ginasios  
Desktop + API Web + Sincronizacao Centralizada

## 2. Visao geral

O sistema centraliza a operacao do ginasio: utentes, contratos, pagamentos,
acessos, caixa, loja, colaboradores, acompanhamento fisico, CRM e comunicacao
por SMS.

## 3. Objetivo do sistema

- Reduzir controlo manual.
- Evitar entradas indevidas.
- Melhorar gestao financeira.
- Acompanhar evolucao dos utentes.
- Fidelizar clientes com CRM, bonus e SMS.
- Preparar o grupo para varias unidades sincronizadas.

## 4. Modulos principais

- Usuarios, perfis e permissoes.
- Utentes e contratos.
- Pacotes e subscricoes.
- Acessos por cartao/tag.
- Avaliacoes fisicas e evolucao.
- Produtos, servicos e vendas.
- Caixa e transacoes financeiras.
- CRM, bonus, campanhas e SMS.
- Sincronizacao com API web.

## 5. Usuarios e permissoes

O sistema permite criar perfis como Gestor, Treinador, Recepcionista, Caixa e
Administrador. Cada perfil recebe uma lista de permissoes, garantindo que cada
colaborador acesse apenas as funcionalidades autorizadas.

## 6. Gestao de utentes

- Cadastro completo do utente.
- Foto e dados de contacto.
- Estado do utente.
- Historico de contratos.
- Historico de pagamentos.
- Historico de acessos.
- Acompanhamento fisico.
- Fidelizacao e bonus.

## 7. Pacotes, subscricoes e contratos

O ginasio pode criar pacotes diarios, semanais, quinzenais, mensais, anuais ou
avulsos. Cada utente fica ligado a um contrato, com datas de inicio e fim,
estado, preco, renovacoes e possiveis taxas de reativacao.

## 8. Controlo de acessos

Os utentes e colaboradores podem entrar com cartao, tag ou outro dispositivo. O
sistema valida contrato, pagamento, dispositivo e regras de acesso antes de
autorizar a entrada na catraca.

## 9. Avaliacao fisica e evolucao

O sistema agenda e regista avaliacoes periodicas do utente, permitindo controlar
peso, medidas, objetivos, observacoes do treinador e proxima data de avaliacao.

## 10. Loja, produtos e servicos

O ginasio pode vender suplementos, agua, equipamentos, aulas extras, servicos de
personal trainer e outros servicos. O sistema controla cadastro, preco, estoque,
vendas e movimentos de produtos/servicos.

## 11. Caixa e transacoes

O caixa regista entradas e saidas financeiras de diferentes origens:

- Pagamentos de mensalidade, anuidade ou planos avulsos.
- Venda de produtos.
- Venda de servicos.
- Reativacao de contratos.
- Ajustes, devolucoes e outras movimentacoes.

## 12. CRM, bonus e SMS

O CRM ajuda a manter o utente ativo e fidelizado:

- Mensagens de boas-vindas.
- Avisos de vencimento.
- SMS para utentes ausentes.
- Lembretes de avaliacao fisica.
- Campanhas promocionais.
- Bonus por fidelizacao.
- Mensagens de aniversario.
- Recuperacao de clientes inativos.

## 13. Criterios para SMS

Exemplos de criterios configuraveis:

- Enviar SMS X dias antes do vencimento do contrato.
- Enviar SMS quando o contrato vencer.
- Enviar SMS se o utente faltar por 7, 15 ou 30 dias.
- Enviar SMS no aniversario.
- Enviar SMS quando houver bonus disponivel.
- Enviar SMS para campanhas ou reativacao.

## 14. Varias unidades do mesmo grupo

Utentes podem frequentar outras unidades do mesmo grupo, respeitando regras
configuraveis. Se os pacotes/precos forem diferentes, o sistema pode limitar o
acesso a uma quantidade configurada de dias, por exemplo 10 dias.

## 15. Desktop, offline e API web

O app desktop sera desenvolvido em C# WPF com arquitetura limpa. Ele podera
operar localmente e sincronizar dados com uma API web centralizada quando houver
internet, mantendo a operacao do ginasio mesmo em cenarios offline.

## 16. Arquitetura proposta

- Dominio: regras centrais do negocio.
- Aplicacao: casos de uso.
- Infraestrutura: banco de dados, API, catraca, SMS e integracoes.
- WPF/UI: telas desktop.
- API Web: dados centralizados, sincronizacao e expansao futura.

## 17. Beneficios para o cliente

- Maior controlo operacional.
- Menos perdas financeiras.
- Melhor experiencia para o utente.
- Decisoes baseadas em dados.
- Mais fidelizacao.
- Preparacao para crescimento em grupo.
- Automatizacao de acessos, comunicacao e pagamentos.

## 18. Fecho

O sistema sera uma plataforma completa para gerir o ginasio de ponta a ponta,
desde a entrada do utente ate ao pagamento, acompanhamento, comunicacao,
fidelizacao e gestao multiunidade.
