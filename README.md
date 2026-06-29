# Aula 01 - Visão Geral e Preparação do Ambiente SQL

## Introdução

Bem-vindos ao nosso workshop sobre SQL e PostgreSQL. Nesta aula, vamos mergulhar nos conceitos básicos de bancos de dados e como o PostgreSQL pode ser utilizado para gerenciar dados de forma eficiente. Nosso objetivo é garantir que todos tenham uma boa base para explorar mais sobre SQL e operações de banco de dados.

## Por que PostgreSQL?

PostgreSQL é um sistema de gerenciamento de banco de dados relacional (RDBMS) desenvolvido no Departamento de Ciência da Computação da Universidade da Califórnia em Berkeley. O POSTGRES foi pioneiro em muitos conceitos que só se tornaram disponíveis em alguns sistemas de banco de dados comerciais muito mais tarde, como:

*   **Consultas complexas**
*   **Chaves estrangeiras (Foreign Keys)**
*   **Triggers**
*   **Views atualizáveis (Updatable Views)**
*   **Integridade transacional**

Além disso, o PostgreSQL pode ser estendido pelo usuário de várias maneiras, por exemplo, adicionando novos tipos de dados, funções, operadores, funções agregadas, métodos de índice e linguagens procedurais.

## Informações Adicionais e Recursos

Para aprofundar seus estudos, recomendo os seguintes recursos:

*   **Documentação Oficial do Postgres**: Contém todas as funcionalidades e detalhes técnicos.
*   **Wiki do PostgreSQL**: Inclui FAQs, lista de tarefas pendentes (TODO) e informações detalhadas sobre diversos tópicos.
*   **Site Oficial do PostgreSQL**: Fornece detalhes sobre a última versão e outras informações úteis.
*   **Comunidade**: O PostgreSQL é um projeto de código aberto. A comunidade de usuários é fundamental para o suporte contínuo. Contribua com seu conhecimento, responda a perguntas nas listas de discussão e compartilhe o que aprender.

## Instalação

Antes de usar o PostgreSQL, é necessário instalá-lo. Ele pode já estar presente em seu sistema operacional ou ter sido instalado pelo administrador. Caso contrário, a instalação é um bom exercício e não é difícil. Para este curso, você pode seguir as instruções para [Instalar o Postgres Localmente](link-para-instrucoes-de-instalacao).

## Fundamentos da Arquitetura

É crucial entender a arquitetura básica do sistema PostgreSQL, que utiliza um modelo cliente/servidor. Compreender essa interação facilitará o uso do banco de dados:

*   **Processo Servidor (`postgres`)**: Gerencia os arquivos do banco de dados, aceita conexões de aplicações cliente e executa ações no banco de dados em nome dos clientes.
*   **Aplicação Cliente (Frontend)**: Realiza operações no banco de dados. Pode ser uma ferramenta de texto, aplicação gráfica, servidor web ou ferramenta de manutenção. O cliente e o servidor podem estar em hosts diferentes, comunicando-se via TCP/IP.

O servidor PostgreSQL pode lidar com múltiplas conexões simultâneas, iniciando um novo processo para cada conexão. O processo servidor supervisor permanece ativo, aguardando novas conexões.

## Criando um Banco de Dados

O primeiro passo é criar um banco de dados. Um servidor PostgreSQL pode gerenciar vários bancos de dados, sendo comum usar um para cada projeto ou usuário. Para isso, utilizaremos o cliente `pgAdmin 4` ou nos conectaremos a servidores remotos como o `Render`.

### Criando nosso Schema com Northwind

Para este projeto, utilizaremos um script SQL simples que preencherá um banco de dados com o famoso exemplo **Northwind**, adaptado para o PostgreSQL. Este script configurará o banco de dados Northwind, criando tabelas e inserindo dados de exemplo, permitindo que você comece a trabalhar imediatamente com consultas e análises SQL em um contexto prático. É uma excelente ferramenta para aprender e praticar operações SQL em um ambiente realista.

## Primeiros Comandos SQL

Vamos a um guia introdutório para operações básicas de SQL utilizando o banco de dados Northwind. Cada comando será explicado para facilitar o entendimento e a aplicação prática.

### Exemplo de Seleção Completa

Para selecionar todos os dados de uma tabela:

```sql
-- Exibe todos os registros da tabela Customers
SELECT * FROM customers;