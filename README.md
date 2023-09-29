# BitBank

Aqui irão as imagens do projeto e correlatos

# Sumário

1. [Descrição do projeto](#project-description)
   - [Introdução](#introduction-project)
   - [Metodologias usadas](#used-methodologies)
2. [Objetivos](#project-objectives)
   - [Objetivo geral](#general-objectives)
   - [Objetivos específicos](#specific-objectives)
3. [Requisitos](#project-requirements)
   - [Requisitos funcionais](#functional-requirements)
   - [Requisitos não funcionais](#non-functional-requirements)
     - [Requisitos de produto](#product-requirements)
     - [Requisitos de organização](#legislation-requirements)
     - [Requisitos de confiabilidade](#confiability-requirements)
     - [Requisito de implementação](#implementation-requirements)
     - [Requisito de padrões](#standard-requirements)
     - [Requisitos de interoperabilidade](#interoperabiliy-requirements)
   - [Banco de dados](#database)
   - [Regras de negócio](#business-rules)
     - [Cheque especial](#overdraft)
     - [Abertura de conta](#account-oppening)
     - [Validações](#validations)
4. [Modelo de dados](#data-model)
   - [Modelo conceitual](#conceptual-model)
   - [Modelo lógico](#logical-model)
     - [Primeiro modelo](#first-model)
     - [Normalização](#normalization)
       - [Primeira forma normal](#first-normal-form)
       - [Segunda forma normal](#second-normal-form)
       - [Terceira forma normal](#third-normal-form)
       - [Forma normal de Boyce-Codd](#boyce-codd-normal-form)
       - [Quarta forma normal](#forth-normal-form)
       - [Quinta forma normal](#fifth-normal-form)
     - [Modelo final](#final-model)
     - [Dicionário de dados](#data-dictionary)
   - [Modelo físico](#physical-model)
5. [Design](#design)
   - [Paleta de cor](#color-palette)
   - [Tipografia](#typography)
   - [Logo](#logo)
   - [Wireframe](#wireframe)
   - [Modelo de navegação](#model-navigation)
6. [Rotas da API](#api-routes)
   - [Validações das rotas](#routes-validation)
7. [Instalação](#instalation)
8. [Contatos](#contact)
9. [Problemas](#issues)

<a id="project-description"></a>

# Descrição do projeto

<a id="introduction-project"></a>

## Introdução

O BitBank surgiu com a ideia inicial de melhorar minhas habilidades com manipulação de banco de dados não relacionais. Mais especificamente, o MongoDB. Porém, com o tempo, viu-se que faria mais sentido para o escopo do projeto e para os meus estudos da faculdade que o banco fosse relacional. Além, é claro, de colocar em prática novas formas de planejamento de projeto.

Assim, venho refazer um projeto antigo. Porém, com grandes melhoras, onde irei utilizar metodologias ágeis como Kanbam e Scrum; além de utilizar um modelo de prototipagem na criação do projeto.

Também haverão melhoras na modelagem de dados do banco. Assim, haverão requisitos que deverão ser seguidos para a realização do MER (Modelo Entidade Relacionamento), diagramatização deste através do DER (Diagrama Entidade Relacionamento), criação de modelos lógicos e físicos. Junto serão criados dicionários de dados do banco, normalizações e tudo que se faz necessário para a criação de um projeto completo.

Com relação ao design, teremos planejamento de paleta de cores, criação de logo, tipografia, modelos de navegação e wireframes para garantir a melhor experiência de navegação.

Em fim, isso e muitas outras melhorias no desenvolvimento e no produto final serão implementadas neste "novo" projeto.
<a id="used-methodologies"></a>

## Metodologias usadas

- Kanbam
- Prototipagem

<a id="project-objectives"></a>

# Objetivos

<a id="general-objectives"></a>

## Objetivo geral

- Desenvolver um software que simulará as ações de um banco e suas movimentações

<a id="specific-objectives"></a>

## Objetivos específicos

1. Desenvolver minhas habilidades de planejamento dos processos de desenvolvimento de softwares
2. Aprender a trabalhar com ferramentas como Kanbam e, até certo ponto, com os conceitos de prototipagem
3. Entender na prática todo o processo de modelagem de dados, indo desde a modelagem conceitual (MER e DER), passando pelo modelo lógico até o modelo físico onde serão concretizados a criação de todas as tabelas do banco
4. Melhorar e entender melhor o meu processo criativo para a criação da paleta de cores, tipografia, logo e distribuição de conteúdos e prototipação de layout com wireframes
5. Adquirir maior pensamento crítico na hora de criar e planejar o modelo de navegação do usuário dentro do software
6. Aprender a utilizar novas ferramentas, como o Sequelize e a sua integração com o MySQL e o mysql2 para criação de querys SQL
7. Aprender a criar documentação com o Swagger para a API feita com o Express e, futuramente, com o Prisma
8. Melhorar meus padrões de commit de código para maior organização e entendimento das diferentes versões do software
9. Desenvolver maior habilidade com manipulação de criptografia de dados, LGPD e Lei Brasileira de Inclusão da Pessoa com Deficiência (LBIPD)
10. Aprender a integrar o plugin VLibre ao software
11. Desenvolver melhores padrões de testes unitários, de integração e E2E (End-to-End) e testes diretos as restrições do banco de dados através do próprio SQL

<a id="project-requirements"></a>

# Requisitos

<a id="functional-requirements"></a>

## Requisitos funcionais

1. Abrir conta
2. Realizar login
3. Efetuar alterações dos dados pessoais do usuário
4. Realizar movimentações financeiras
5. Criar QrCodes para realizar cobranças
6. Criar relatórios do histórico de todas as transações do usuário
7. Filtrar relatórios por datas
8. Inativar contas sem movimentação por 1 mês
9. Consultar dados bancários
10. Consultar CPF na Receita Federal
11. Consultar endereço na API da ViaCep
12. Consultar cotação de moedas na API da Caixa Econômica Federal

<a id="non-functional-requirements"></a>

## Requisitos não funcionais

<a id="product-requirements"></a>

### Requisitos de produto

1. O software deve ser capaz de rodar em todas os sistemas operacionais através da web
2. Deve haver compatibilidade entre a forma que o software roda nos diferentes browsers, sendo os principais:

   [![Edge](https://img.shields.io/badge/Edge-0078D7?style=for-the-badge&logo=Microsoft-edge&logoColor=white)](https://www.microsoft.com/pt-br/edge?form=MA13FJ)
   [![Firefox](https://img.shields.io/badge/Firefox-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white)](https://www.mozilla.org/pt-BR/firefox/new/)
   [![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white)](https://www.google.com/chrome/)
   [![Safari](https://img.shields.io/badge/Safari-000000?style=for-the-badge&logo=Safari&logoColor=white)](https://www.apple.com/br/safari/)
   [![Opera](https://img.shields.io/badge/Opera-FF1B2D?style=for-the-badge&logo=Opera&logoColor=white)](https://www.opera.com/gx?utm_id=EAIaIQobChMItPmdnY6-gQMV9AutBh1DBAK-EAAYAiAAEgLDzPD_BwE&utm_medium=pa&utm_source=google&utm_campaign=OGX_BR_Search_EN_T4_Competitors_V2&utm_content=639990942371&gad=1&gclid=EAIaIQobChMItPmdnY6-gQMV9AutBh1DBAK-EAAYAiAAEgLDzPD_BwE)

<a id="legislation-requirements"></a>

### Requisitos de legislação

1. Garantir integralmente todos os artigos do LGPD (Lei Geral de Proteção de Dados)
2. Garantir acessibilidade do softwrae de acordo com a LBIPD (Lei Brasileira de Inclusão da Pessoa com Deficiência)

<a id="confiability-requirements"></a>

### Requisitos de confiabilidade

1. O software deve estar em funcionamento 99% do tempo, com excessão de funcionalidade que:
   - Usem ferramentas que necessitem de validação do CPF através da Receita Federal

<a id="implementation-requirements"></a>

### Requisitos de implementação

1. O sofwtare deverá ser implementado com as seguintes tecnologias:

   [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
   [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
   [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://devdocs.io/javascript/)
   [![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=Sequelize&logoColor=white)](https://sequelize.org/)
   [![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)](https://expressjs.com/)
   [![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)](https://dev.mysql.com/doc/)
   [![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/en/docs)
   [![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)](https://nodemon.io/)
[![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white)](https://jestjs.io/docs/getting-started)
[![cypress](https://img.shields.io/badge/-cypress-%23E5E5E5?style=for-the-badge&logo=cypress&logoColor=058a5e)](https://docs.cypress.io)

2. Pretende-se, futuramente, migrar o software para as seguintes tecnologias:

   [![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)](https://angular.io/docs)
   [![RxJS](https://img.shields.io/badge/rxjs-%23B7178C.svg?style=for-the-badge&logo=reactivex&logoColor=white)](https://rxjs.dev/guide/overview)
   [![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/docs/)
   [![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white)](https://sass-lang.com/documentation/)
   [![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)](https://www.prisma.io/docs)
   [![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)](https://expressjs.com/)
   [![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)](https://dev.mysql.com/doc/)
   [![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/en/docs)
   [![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)](https://nodemon.io/)
[![Jasmine](https://img.shields.io/badge/jasmine-%238A4182.svg?style=for-the-badge&logo=jasmine&logoColor=white)](https://jasmine.github.io/)

<a id="standard-requirements"></a>

### Requisitos de padrão

Irão ser usados os seguintes padrões de código:

1. [Orientação a objeto](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_programming)
2. [SOLID](https://www.treinaweb.com.br/blog/principios-solid-single-responsability-principle)
3. [Clean Code](https://balta.io/artigos/clean-code)

<a id="interoperabiliy-requirements"></a>

### Requisitos de interoperabilidade

O software irá se comunicar com

1. MySQL
2. API's externas, como: ViaCep, API da Receita Federal e API da Caixa Econômica

<a id="database"></a>

### Banco de dados

1. Uma pessoa deve ter:

   - CPF exclusivo
   - Nome completo formado por nome e sobrenome
   - Data de nascimento
   - Idade
   - Endereço formado por CEP, logradouro, complemento (que pode ou não existir), bairro, localidade e UF
   - Sexo, podendo ser M (Masculino) ou F (Feminino)
   - Nacionalidades
   - Estado civil
   - Telefones formados por DDD e número
   - Foto

2. Uma pessoa pode fazer:

   - Cadastro no sistema
   - Ao se cadastrar, devem ficar armazenados os seguintes dados: data e hora do cadastro e cpf de quem se cadastrou
   - Ao se cadastrar a pessoa se torna, automaticamente, um usuário do sistema
   - Uma pessoa pode cadastrar apenas 1 usuário

3. Um usuário deve possuir:

   - Comprovante de renda
   - E-mail exclusivo
   - Uma ou nenhuma conta bancária

4. Um usuário pode fazer:

   - Transferência de valores monetários para outros usuários
   - Sacar ou depositar valores monetários na sua própria conta

5. Toda conta bancária deve possuir:

   - Número de conta exclusivo
   - Agência
   - Saldo
   - Cheque especial
   - Toda conta pode ser de um dos três tipos: corrente, salário ou poupança ou até mesmo um conjunto de um ou mais tipos de conta
   - Cada tipo de conta deve ter um identificador que a represente
   - Uma conta pode ter um usuário associado e também pode ser movimentada por meio de saques e depósitos também por apenas um usuário

6. Toda transação deve ficar armazenada (formando um histórico de cada usuário) e conter as seguintes informações:

   - Usuário que realizou a movimentação
   - Usuário que recebeu a movimentação caso exista
   - A data da movimentação
   - O valor que foi movimentado
   - O status da movimentação (permitida, bloqueada)
   - Caso tenha sido bloqueada, o motivo do bloqueio da movimentação

<a id="business-rules"></a>

## Regras de negócio

<a id="overdraft"></a>

### Cheque especial

1. Para pessoas com renda abaixo de 1500, o cheque especial deve ser nulo
2. Para pessoas com renda abaixo de 2500, o cheque especial deve ser de 35%
3. Para pessoas com renda a cima de 2500, o cheque especial deve ser de 50%

<a id="account-oppening"></a>

### Abertura de conta

1. Para que a abertura de conta seja permitida, é necessário que o usuário tenha seu CPF totalmente regularizado, ou seja, sem pendências no Serasa, Receita Federal e afins
2. O usuário precisa ter no mínimo 18 anos para abrir uma conta bancária
3. As contas bancárias podem ser dos tipos: corrente, salário ou poupança

<a id="validations"></a>

### Validações

1. A validação de usuário para login deve ser feita em duas etapas. As opções de validação são:
   - O usuário pode validar seu login com sua senha e com um e-mail enviado de forma automática com um código de segurança de 8 caracteres aleatórios
   - O usuário pode validar seu login com sua senha e uma imagem de perfil
   - Com sua senha e um SMS enviado para o número de telefone cadastrado com um código de segurança de 8 caracteres aleatórios
2. Toda senha precisa ter, no mínimo, 14 caracteres que contenham:
   - No mínimo uma letra maiúscula
   - No mínimo uma letra minúscula
   - No mínimo um caractere especial
   - No mínimo um dígito numérico
   - Não podem haver dígitos numéricos sequenciais, tais como 12 ou 45
3. Ainda com relação as senhas, temos que outras validações deverão ser feitas, tais como:
   - A entropia de toda senha registrada deve ter, no mínimo, um valor de 92.4 bits
   - Deve haver um dicionários de senhas vulneráveis
   - Deste dicionário, deve-se verificar se a senha a ser cadastrada possui, parcial ou inteiramente, algum padrão registrado no dicionário de senhas
4. Para criação de conta, é obrigatório que o usuário tire uma foto do seu rosto para futuras validações e maior segurança
5. Todas as transações efetuadas podem ser feitas no débito, ou seja, debitadas imediatamente ou no formato de crédito (a transação é parcelada em até 12x para quem efetuar a transação) e inserida de forma total e integral na conta de quem receber essa transação
6. As contas correntes podem executar saques, transferências e depósitos
7. As contas salários podem executar transferências e depósitos
8. As contas popanças só podem executar depósitos e saques

<a id="data-model"></a>

# Modelo de dados

<a id="conceptual-model"></a>

## Modelo conceitual

<a id="logical-model"></a>

## Modelo lógico

<a id="first-model"></a>

### Primeiro modelo

<a id="normalization"></a>

### Normalização

<a id="first-normal-form"></a>

#### Primeira forma normal

<a id="second-normal-form"></a>

#### Segunda forma normal

<a id="third-normal-form"></a>

#### Terceira forma normal

<a id="boyce-codd-normal-form"></a>

#### Forma normal de Boyce-Codd

<a id="forth-normal-form"></a>

#### Quarta forma normal

<a id="fifth-normal-form"></a>

#### Quinta forma normal

<a id="final-model"></a>

### Modelo final

<a id="data-dictionary"></a>

### Dicionário de dados

<a id="physical-model"></a>

## Modelo físico

<a id="design"></a>

# Design

<a id="color-palette"></a>

## Paleta de cor

<a id="typography"></a>

## Tipografia

<a id="logo"></a>

## Logo

<a id="wireframe"></a>

## Wireframe

<a id="model-navigation"></a>

## Modelo de navegação

<a id="routes-api"></a>

# Rotas da API

<a id="routes-validation"></a>

## Validação das rotas

<a id="instalation"></a>

# Instalação

<a id="contact"></a>

# Contatos

<a id="issues"></a>

# Problemas
