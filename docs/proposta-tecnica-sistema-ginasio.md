# Proposta Técnica - Sistema de Gestão para Ginásios

## 1. Visão geral

Esta proposta descreve a evolução do sistema de gestão para ginásios em três
etapas. A solução começa como uma aplicação desktop em C# WPF, mantendo a
arquitetura limpa já existente, e evolui depois para API web, painel remoto,
CRM e aplicação mobile para os utentes.

O objetivo é entregar primeiro uma base operacional sólida para o ginásio
funcionar no dia a dia, sem depender inicialmente de Web API, CRM, mobile ou
integrações entre ginásios.

## 2. Premissas consideradas

- Já existe uma base forte de aplicação em arquitetura limpa.
- A estrutura de UI WPF será mantida e adaptada ao domínio do ginásio.
- O trabalho inicial será principalmente de adaptação, criação de entidades,
  regras de negócio, telas, fluxos e testes.
- A primeira etapa não inclui CRM, Web API, aplicação mobile nem integração com
  outros ginásios.
- A primeira etapa inclui backup na nuvem.
- As estimativas abaixo consideram uma rotina de trabalho de 9 horas por dia,
  5 dias por semana.
- As estimativas são em dias de trabalho, não dias corridos.

## 3. Divisão por etapas

### Etapa 1 - Sistema desktop base

#### Objetivo

Entregar uma versão desktop operacional para o ginásio gerir a sua operação
principal localmente, com backup na nuvem, sem depender de Web API, CRM, mobile
ou integração com outras unidades.

#### Inclui

- Aplicação desktop em C# WPF.
- Manutenção da arquitetura limpa existente.
- Adaptação da UI existente para o domínio de ginásio.
- Usuários do sistema.
- Perfis e permissões.
- Configurações gerais.
- Cadastro de utentes.
- Pacotes/subscrições: diário, semanal, quinzenal, mensal, anual e avulso.
- Contratos dos utentes.
- Pagamentos de subscrições.
- Caixa e transações financeiras.
- Cadastro de produtos e serviços.
- Vendas de produtos e serviços.
- Movimentos de produtos e serviços.
- Avaliações físicas/check-ups.
- Dispositivos de acesso, como cartões ou tags.
- Registo de acessos de utentes e colaboradores.
- Relatórios básicos.
- Backup na nuvem.

#### Não inclui nesta etapa

- CRM.
- Envio automático de SMS.
- Web API.
- Painel web.
- App mobile.
- Integração entre ginásios do mesmo grupo.
- Sincronização centralizada com servidor.

#### Estimativa

**25 a 40 dias de trabalho.**

Esta etapa é a mais importante, porque cria a base operacional do sistema. A
estimativa fica menor porque a arquitetura limpa e a UI já existem, mas ainda
existem fluxos sensiveis como caixa, contratos, pagamentos, acessos, backup e
permissões.

### Etapa 2 - Web API, painel web e CRM

#### Objetivo

Adicionar uma camada web para centralizar dados, permitir monitoramento remoto
do ginásio, habilitar CRM e preparar o sistema para operação multiunidade.

#### Inclui

- Web API em ASP.NET Core.
- Banco de dados central.
- Autenticação e autorização na API.
- Sincronização entre desktop e servidor.
- Painel web para monitoramento remoto.
- Dashboards de utentes, contratos, pagamentos, acessos, vendas e caixa.
- CRM.
- Campanhas.
- Bónus e fidelização.
- Integração com provedor SMS.
- Mensagens automáticas por critérios configuraveis.
- Preparação para regras entre ginásios do mesmo grupo.

#### Exemplos de critérios para SMS

- Boas-vindas ao cadastrar utente.
- Aviso antes do vencimento do contrato.
- Aviso de contrato vencido.
- Mensagem para utentes ausentes.
- Lembrete de avaliação física.
- Aniversário do utente.
- Bónus ou campanha promocional.
- Reativação de clientes inativos.

#### Estimativa

**25 a 40 dias de trabalho.**

O ponto mais sensivel destá etapa e a sincronização entre o desktop e a API,
porque será necessario garantir consistência dos dados, histórico de alteráções,
segurança e tratamento de conflitos.

### Etapa 3 - Aplicação mobile para utentes

#### Objetivo

Disponibilizar uma aplicação mobile para que cada utente acompanhe os seus dados
e interájá com o ginásio de forma mais autónoma.

#### Inclui

- Login do utente.
- Visualizacao do contrato atual.
- Validade da subscrição.
- Histórico de pagamentos.
- Histórico de acessos.
- Evolucao física e avaliações.
- Visualizacao de bónus e campanhas.
- Notificacoes.
- Possibilidade de pagamentos, se houver gateway definido.

#### Estimativa

**20 a 30 dias de trabalho.**

Se a aplicação mobile for apenas de consulta, tende a ficar mais próxima do
limite inferior. Se incluir pagamentos online, notificações push, documentos,
publicacao em lojas e recursos avançados, apróxima-se do limite superior.

## 4. Resumo das estimativas

| Etapa | Escopo principal | Estimativa |
| --- | --- | ---: |
| Etapa 1 | Desktop base com backup na nuvem | 25 a 40 dias |
| Etapa 2 | Web API, painel web e CRM | 25 a 40 dias |
| Etapa 3 | App mobile para utentes | 20 a 30 dias |
| **Total** | Sistema completo nas três etapas | **70 a 110 dias** |

## 5. Conversão para semanas de trabalho

Considerando 5 dias de trabalho por semana:

| Etapa | Equivalente aproximado |
| --- | ---: |
| Etapa 1 | 5 a 8 semanas |
| Etapa 2 | 5 a 8 semanas |
| Etapa 3 | 4 a 6 semanas |
| **Total** | **14 a 22 semanas** |

## 6. Observações importantes

As estimativas podem variar conforme:

- nível de acabamento visual exigido;
- quantidade de relatórios;
- complexidade da catraca/cartões/tags;
- regras específicas de caixa e recibos;
- modelo de backup na nuvem;
- gateway de pagamentos escolhido no mobile;
- quantidade de permissões e perfis;
- necessidade de importação de dados existentes;
- exigências fiscais ou legais locais.

## 7. Recomendação de execução

A recomendação é iniciar pela Etapa 1 como MVP operacional. Esta etapa deve
entregar valor real ao ginásio, permitindo gerir utentes, contratos, pagamentos,
caixa, produtos, acessos e avaliações físicas.

Depois da Etapa 1 estabilizada, a Etapa 2 deve adicionar a API, o painel web e
o CRM. Por fim, a Etapa 3 deve entregar a experiência mobile para os utentes.

## 8. Resumo executivo

Com a base atual já existente em arquitetura limpa e UI WPF, o sistema completo
pode ser planeado em três etapas:

- **Etapa 1:** desktop operacional em 25 a 40 dias de trabalho.
- **Etapa 2:** Web API, painel web e CRM em 25 a 40 dias de trabalho.
- **Etapa 3:** app mobile para utentes em 20 a 30 dias de trabalho.

O total estimado fica entre **70 e 110 dias de trabalho**, considerando uma
rotina de 9 horas por dia e 5 dias por semana.
