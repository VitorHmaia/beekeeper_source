# API para Coleta de Dados sobre Abelhas e Colmeias

## Introdução

### Visão Geral do Projeto

Esta API é projetada para coletar dados sobre abelhas e colmeias, exibindo essas informações em um dashboard para monitoramento.

### Objetivos e Propósito do Sistema

- A API irá receber dados para exibição em um dashboard para monitoramento da colmeia.

### Benefícios Esperados do Projeto

- Melhoria do controle de ambiente da colmeia.
- Decisões mais assertivas para aumentar a produtividade de mel das abelhas.

## Visão Geral do Sistema

### Descrição do Sistema

O sistema será desenvolvido seguindo o padrão de arquitetura MVC (Model-View-Controller), com um frontend para exibição do dashboard, backend para atender as requisições MQTT enviadas via simulação, e acesso ao banco de dados SQL via ORM e padrão Repository.

### Público-Alvo do Sistema

- Apicultores que desejam melhorar sua produção de mel utilizando tecnologia IoT e TI.

## Requisitos Funcionais e Não Funcionais

### Requisitos Funcionais

- Conhecimento em Nest.JS para desenvolvimento do backend da API, com os módulos necessários para controle dos endpoints (versão alvo não decidida).
- Conhecimento em Prisma para utilizar como ORM e comunicação com o banco de dados (versão alvo não decidida).
- Conhecimento em React.js para criação do frontend da API e modularização dos componentes (versão alvo não decidida).
- Conhecimento em Next.js para trabalhar junto com React.js no frontend (versão alvo não decidida).
- Banco de Dados a ser decidido.
- Docker para build da aplicação (versão alvo não decidida).
- Conhecimento em comandos Git para versionamento do código fonte e controle do repositório (versão alvo não decidida).
- GitHub para disponibilização do repositório remoto e controle de versionamento.
- Conhecimento em comandos Bash/Shell para uso de CLI para as ferramentas mencionadas.
- Conhecimento em Broker MQTT e seu protocolo de comunicação.
- Conhecimento em TLS para camada de segurança da aplicação web.

### Requisitos Não Funcionais

- Lógica de programação.
- Algoritmos.
- Banco de Dados.
- Redes.

## Arquitetura do Sistema

### Explicação da Arquitetura MVC

- **Model**: Gerencia a lógica dos dados e as regras de negócios.
- **View**: Exibe os dados ao usuário e envia comandos de usuário ao Controller.
- **Controller**: Interpreta as entradas do usuário e mapeia para ações no Model ou na View.

### Uso do Padrão Repository

- Implementação do padrão Repository para acesso a dados de forma desacoplada e organizada.

## Requisitos Funcionais

- Lista detalhada de funcionalidades do sistema.
- Casos de uso principais.
- Fluxos de trabalho do usuário.

## Requisitos Não Funcionais

- Desempenho esperado do sistema.
- Segurança e autenticação.
- Escalabilidade e manutenibilidade.

## Tecnologias Utilizadas

### Linguagens de Programação

- TypeScript (TS)
- JavaScript (JS)

### Frameworks

- React.js
- Next.js
- Nest.JS

### Bancos de Dados

- A ser decidido.

### Ferramentas de Desenvolvimento

- Git
- Docker

## Modelo de Dados

- Estrutura do banco de dados.
- Relacionamentos entre entidades.
- Esquema de armazenamento.

## Interfaces do Usuário

- Layout e design das interfaces.
- Funcionalidades específicas de cada tela.
- Fluxos de interação do usuário.

## Arquitetura de Implementação

- Organização do código-fonte.
- Divisão em módulos e componentes.
- Dependências entre os componentes.

## Planejamento de Implantação (Vitor Maia)

- Ambientes de implantação (dev, teste, produção).
- Procedimentos de implantação.
- Migração de dados, se necessário.

## Gestão de Configuração e Controle de Versão

- Políticas de controle de versão.
- Ramificação do código-fonte.
- Uso de ferramentas de controle de versão (ex: Git).

## Gestão de Projetos

- Cronograma de desenvolvimento.
- Atribuição de tarefas e responsabilidades.
- Monitoramento do progresso do projeto.

## Considerações de Segurança (Carlos)

- Mecanismos de autenticação e autorização.
- Proteção contra vulnerabilidades conhecidas.
- Auditoria e registro de atividades sensíveis.

## Considerações de Manutenção

- Planos de suporte pós-implantação.
- Processo de correção de bugs e implementação de melhorias.
- Atualizações de segurança e de software.

### Ambientes de Implantação:

- Configurar ambos os ambientes, desenvolvimento (Dev) e produção (Prod), na mesma máquina para simplificar o gerenciamento.
- Utilizar diferentes portas ou nomes de host para acessar os ambientes, por exemplo, localhost:3000 para Dev e localhost:4000 para Prod.

### Procedimentos de Implantação:

#### Para o ambiente de desenvolvimento:

- Utilizar Docker Compose para orquestrar os contêineres em um único nó Docker Swarm dedicado ao ambiente de desenvolvimento.
- Configurar o acesso aos serviços do ambiente de desenvolvimento apenas localmente para garantir a segurança.

#### Para o ambiente de produção:

- Deploy em VM free tier Oracle com Linux e configuração de redes e do serviço para receber acesso com port forwarding.

### Migração de Dados, se Necessário:

- Desenvolver scripts de migração de dados compatíveis com o Docker Swarm que possam ser executados na mesma máquina.
- Utilizar volumes persistentes do Docker Swarm para armazenar dados compartilhados entre os serviços em ambientes de desenvolvimento e produção.

### Gestão de Configuração e Controle de Versão:

#### Política de Versão (SemVer):

- Adotar o Semantic Versioning (SemVer) como política de versionamento para o seu projeto.
- Seguir a estrutura MAJOR.MINOR.PATCH para versionamento, onde:
  - Incrementos MAJOR são para mudanças incompatíveis com versões anteriores.
  - Incrementos MINOR são para adições compatíveis com versões anteriores.
  - Incrementos PATCH são para correções de bugs compatíveis com versões anteriores.

#### Ramificação do Código-fonte (GitFlow):

- Utilizar o GitFlow como modelo de ramificação para organizar o fluxo de trabalho, com branches principais para feature, develop, release e master.
- Desenvolver novas funcionalidades em branches de feature, integrá-las ao branch develop e, após testes adequados, fazer o merge para o branch release e, eventualmente, para o branch master.

#### Uso de Ferramentas de Controle de Versão (Git):

- Utilizar o Git como a principal ferramenta de controle de versão, seguindo os princípios do GitFlow e do padrão de commit Conventional Commits dentro do GitHub.


---

Este README fornece uma visão abrangente do projeto de uma API para coleta de dados sobre abelhas e colmeias, incluindo a descrição do sistema, requisitos, arquitetura e planejamento de implantação. Para mais detalhes, consulte a documentação específica de cada módulo e componente.
