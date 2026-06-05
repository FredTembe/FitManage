# Proposta Tecnica - Sistema de Gestao para Ginasios

## 1. Visao geral

Esta proposta descreve a evolucao do sistema de gestao para ginasios em tres
etapas. A solucao comeca como uma aplicacao desktop em C# WPF, mantendo a
arquitetura limpa ja existente, e evolui depois para API web, painel remoto,
CRM e aplicacao mobile para os utentes.

O objetivo e entregar primeiro uma base operacional solida para o ginasio
funcionar no dia a dia, sem depender inicialmente de Web API, CRM, mobile ou
integracoes entre ginasios.

## 2. Premissas consideradas

- Ja existe uma base forte de aplicacao em arquitetura limpa.
- A estrutura de UI WPF sera mantida e adaptada ao dominio do ginasio.
- O trabalho inicial sera principalmente de adaptacao, criacao de entidades,
  regras de negocio, telas, fluxos e testes.
- A primeira etapa nao inclui CRM, Web API, aplicacao mobile nem integracao com
  outros ginasios.
- A primeira etapa inclui backup na nuvem.
- As estimativas abaixo consideram uma rotina de trabalho de 9 horas por dia,
  5 dias por semana.
- As estimativas sao em dias de trabalho, nao dias corridos.

## 3. Divisao por etapas

### Etapa 1 - Sistema desktop base

#### Objetivo

Entregar uma versao desktop operacional para o ginasio gerir a sua operacao
principal localmente, com backup na nuvem, sem depender de Web API, CRM, mobile
ou integracao com outras unidades.

#### Inclui

- Aplicacao desktop em C# WPF.
- Manutencao da arquitetura limpa existente.
- Adaptacao da UI existente para o dominio de ginasio.
- Usuarios do sistema.
- Perfis e permissoes.
- Configuracoes gerais.
- Cadastro de utentes.
- Pacotes/subscricoes: diario, semanal, quinzenal, mensal, anual e avulso.
- Contratos dos utentes.
- Pagamentos de subscricoes.
- Caixa e transacoes financeiras.
- Cadastro de produtos e servicos.
- Vendas de produtos e servicos.
- Movimentos de produtos e servicos.
- Avaliacoes fisicas/check-ups.
- Dispositivos de acesso, como cartoes ou tags.
- Registo de acessos de utentes e colaboradores.
- Relatorios basicos.
- Backup na nuvem.

#### Nao inclui nesta etapa

- CRM.
- Envio automatico de SMS.
- Web API.
- Painel web.
- App mobile.
- Integracao entre ginasios do mesmo grupo.
- Sincronizacao centralizada com servidor.

#### Estimativa

**25 a 40 dias de trabalho.**

Esta etapa e a mais importante, porque cria a base operacional do sistema. A
estimativa fica menor porque a arquitetura limpa e a UI ja existem, mas ainda
existem fluxos sensiveis como caixa, contratos, pagamentos, acessos, backup e
permissoes.

### Etapa 2 - Web API, painel web e CRM

#### Objetivo

Adicionar uma camada web para centralizar dados, permitir monitoramento remoto
do ginasio, habilitar CRM e preparar o sistema para operacao multiunidade.

#### Inclui

- Web API em ASP.NET Core.
- Banco de dados central.
- Autenticacao e autorizacao na API.
- Sincronizacao entre desktop e servidor.
- Painel web para monitoramento remoto.
- Dashboards de utentes, contratos, pagamentos, acessos, vendas e caixa.
- CRM.
- Campanhas.
- Bonus e fidelizacao.
- Integracao com provedor SMS.
- Mensagens automaticas por criterios configuraveis.
- Preparacao para regras entre ginasios do mesmo grupo.

#### Exemplos de criterios para SMS

- Boas-vindas ao cadastrar utente.
- Aviso antes do vencimento do contrato.
- Aviso de contrato vencido.
- Mensagem para utentes ausentes.
- Lembrete de avaliacao fisica.
- Aniversario do utente.
- Bonus ou campanha promocional.
- Reativacao de clientes inativos.

#### Estimativa

**25 a 40 dias de trabalho.**

O ponto mais sensivel desta etapa e a sincronizacao entre o desktop e a API,
porque sera necessario garantir consistencia dos dados, historico de alteracoes,
seguranca e tratamento de conflitos.

### Etapa 3 - Aplicacao mobile para utentes

#### Objetivo

Disponibilizar uma aplicacao mobile para que cada utente acompanhe os seus dados
e interaja com o ginasio de forma mais autonoma.

#### Inclui

- Login do utente.
- Visualizacao do contrato atual.
- Validade da subscricao.
- Historico de pagamentos.
- Historico de acessos.
- Evolucao fisica e avaliacoes.
- Visualizacao de bonus e campanhas.
- Notificacoes.
- Possibilidade de pagamentos, se houver gateway definido.

#### Estimativa

**20 a 30 dias de trabalho.**

Se a aplicacao mobile for apenas de consulta, tende a ficar mais proxima do
limite inferior. Se incluir pagamentos online, notificacoes push, documentos,
publicacao em lojas e recursos avancados, aproxima-se do limite superior.

## 4. Resumo das estimativas

| Etapa | Escopo principal | Estimativa |
| --- | --- | ---: |
| Etapa 1 | Desktop base com backup na nuvem | 25 a 40 dias |
| Etapa 2 | Web API, painel web e CRM | 25 a 40 dias |
| Etapa 3 | App mobile para utentes | 20 a 30 dias |
| **Total** | Sistema completo nas tres etapas | **70 a 110 dias** |

## 5. Conversao para semanas de trabalho

Considerando 5 dias de trabalho por semana:

| Etapa | Equivalente aproximado |
| --- | ---: |
| Etapa 1 | 5 a 8 semanas |
| Etapa 2 | 5 a 8 semanas |
| Etapa 3 | 4 a 6 semanas |
| **Total** | **14 a 22 semanas** |

## 6. Observacoes importantes

As estimativas podem variar conforme:

- nivel de acabamento visual exigido;
- quantidade de relatorios;
- complexidade da catraca/cartoes/tags;
- regras especificas de caixa e recibos;
- modelo de backup na nuvem;
- gateway de pagamentos escolhido no mobile;
- quantidade de permissoes e perfis;
- necessidade de importacao de dados existentes;
- exigencias fiscais ou legais locais.

## 7. Recomendacao de execucao

A recomendacao e iniciar pela Etapa 1 como MVP operacional. Esta etapa deve
entregar valor real ao ginasio, permitindo gerir utentes, contratos, pagamentos,
caixa, produtos, acessos e avaliacoes fisicas.

Depois da Etapa 1 estabilizada, a Etapa 2 deve adicionar a API, o painel web e
o CRM. Por fim, a Etapa 3 deve entregar a experiencia mobile para os utentes.

## 8. Resumo executivo

Com a base atual ja existente em arquitetura limpa e UI WPF, o sistema completo
pode ser planeado em tres etapas:

- **Etapa 1:** desktop operacional em 25 a 40 dias de trabalho.
- **Etapa 2:** Web API, painel web e CRM em 25 a 40 dias de trabalho.
- **Etapa 3:** app mobile para utentes em 20 a 30 dias de trabalho.

O total estimado fica entre **70 e 110 dias de trabalho**, considerando uma
rotina de 9 horas por dia e 5 dias por semana.
