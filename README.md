# BitBank
Aqui irão as imagens do projeto e correlatos

# Sumário
1. [Descrição do projeto](#project-description)
	* [Introdução](#introduction-project)
	* [Metodologias usadas](#used-methodologies)
2. [Objetivos](#project-objectives)
	* [Objetivo geral](#general-objectives)
	* [Objetivos específicos](#specific-objectives)
3. [Requisitos](#project-requirements)
	* [Requisitos funcionais](#functional-requirements)
	* [Requisitos não funcionais](#non-functional-requirements)
		* [Requisitos de produto](#product-requirements)
		* [Requisitos de organização](#legislation-requirements)
		* [Requisitos de confiabilidade](#confiability-requirements)
		* [Requisito de implementação](#implementation-requirements)
		* [Requisito de padrões](#standard-requirements)
		* [Requisitos de interoperabilidade](#interoperabiliy-requirements)
	* [Banco de dados](#database)
	* [Regras de negócio](#business-rules)
		* [Cheque especial](#overdraft)
		* [Abertura de conta](#account-oppening)
		* [Validações](#validations)
		* [Impostos](#tax)
4. [Modelo de dados](#data-model)
	* [Modelo conceitual](#conceptual-model)
	* [Modelo lógico](#logical-model)
	* [Físico](#physical-model)
5. [Design](#design)
	* [Paleta de cor](#color-palette)
	* [Tipografia](#typography)
	* [Logo](#logo)
	* [Wireframe](#wireframe)
	* [Modelo de navegação](#model-navigation)
6. [Rotas da API](#api-routes)
	* [Validações das rotas](#routes-validation)
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
* Kanbam
* Scrum
* Prototipagem

<a id="project-objectives"></a>
# Objetivos

<a id="general-objectives"></a>
## Objetivo geral
* Desenvolver um software que simulará as ações de um banco e suas movimentações

<a id="specific-objectives"></a>
## Objetivos específicos
1. Desenvolver minhas habilidades de planejamento dos processos de desenvolvimento de softwares
2. Aprender a trabalhar com ferramentas como Kanbam e, até certo ponto, com os conceitos do Scrum e de prototipagem
3. Entender na prática todo o processo de modelagem de dados, indo desde a modelagem conceitual (MER e DER), passando pelo modelo lógico até o modelo físico onde serão concretizados a criação de todas as tabelas do banco
4. Melhorar e entender melhor o meu processo criativo para a criação da paleta de cores, tipografia, logo e distribuição de conteúdos e prototipação de layout com wireframes
5. Adquirir maior pensamento crítico na hora de criar e planejar o modelo de navegação do usuário dentro do software
6. Aprender a utilizar novas ferramentas, como o Sequelize e a sua integração com o MySQL e o mysql2 para criação de querys SQL
7. Aprender a criar documentação com o Swagger para a API feita com o Express
8. Melhorar meus padrões de commit de código para maior organização e entendimento das diferentes versões do software
9. Desenvolver maior habilidade com manipulação de criptografia de dados, LGPD e Lei Brasileira de Inclusão da Pessoa com Deficiência (LBIPD)
10. Aprender a integrar o plugin VLibre ao software

<a id="project-requirements"></a>
# Requisitos

<a id="functional-requirements"></a>
## Requisitos funcionais
1. Cadastrar usuários para abrir conta
2. Realizar login
3. Efetuar mudanças dos dados pessoais da conta do usuário
4. Deve ser possível realizar movimentações financeiras, como:
	* Depósitos
	* Saques
	* Transferências entre contas distintas
5. Deve ser possível criar QrCodes para realizar cobranças
6. Deve ser possível criar relatórios do histórico de todas as transações do usuário, com filtros de data inicial e data final
7. O usuário pode escolher fechar a sua conta bancária
8. O BitBank irá fechar toda conta inativa por mais de 1 mes
9. O usuário deve poder realizar consultas no seu saldo bancário e em todos os dados da sua conta

<a id="non-functional-requirements"></a>
## Requisitos não funcionais

<a id="product-requirements"></a>
### Requisitos de produto
1. O software deve ser capaz de rodar em todas os sistemas operacionais através da web
2. Deve haver compatibilidade entre a forma que o software roda nos diferentes browsers, sendo os principais:

	![Edge](https://img.shields.io/badge/Edge-0078D7?style=for-the-badge&logo=Microsoft-edge&logoColor=white)
	![Firefox](https://img.shields.io/badge/Firefox-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white)
	![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white)
	![Safari](https://img.shields.io/badge/Safari-000000?style=for-the-badge&logo=Safari&logoColor=white)
	![Opera](https://img.shields.io/badge/Opera-FF1B2D?style=for-the-badge&logo=Opera&logoColor=white)

<a id="legislation-requirements"></a>
### Requisitos de legislação
1. Garantir integralmente todos os artigos do LGPD (Lei Geral de Proteção de Dados)
2. Garantir acessibilidade do softwrae de acordo com a LBIPD (Lei Brasileira de Inclusão da Pessoa com Deficiência)

<a id="confiability-requirements"></a>
### Requisitos de confiabilidade
1. O software deve estar em funcionamento 99% do tempo, com excessão de funcionalidade que:
	* Usem ferramentas que necessitem de validação do CPF através da Receita Federal

<a id="implementation-requirements"></a>
### Requisitos de implementação
1. O sofwtare deverá ser implementado com as seguintes tecnologias:

	![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
	![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
	![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
	![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=Sequelize&logoColor=white)
	![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
	![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
	![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
	![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)

2. Pretende-se, futuramente, migrar o software para as seguintes tecnologias:

	![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)
	![RxJS](https://img.shields.io/badge/rxjs-%23B7178C.svg?style=for-the-badge&logo=reactivex&logoColor=white)
	![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
	![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white)
	![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)
	![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
	![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
	![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
	![Nodemon](https://img.shields.io/badge/NODEMON-%23323330.svg?style=for-the-badge&logo=nodemon&logoColor=%BBDEAD)

<a id="standard-requirements"></a>
### Requisitos de padrão
Irão ser usados os seguintes padrões de código:

1. Orientação a objeto
2. [SOLID](https://www.treinaweb.com.br/blog/principios-solid-single-responsability-principle)
3. [Clean Code](https://balta.io/artigos/clean-code)

<a id="interoperabiliy-requirements"></a>
### Requisitos de interoperabilidade
O software irá se comunicar com

1. MySQL
2. API's externas, como: ViaCep, API da Receita Federal e API da Caixa Econômica
	
<a id="database"></a>
## Banco de dados
1. Todo usuário deve possuir:
	* Nome completo formado por nome e sobrenome
	* CPF único e exclusivo
	* E-mail único e exclusivo
	* Nacionalidade
	* Data de nascimento
	* Idade
	* Um ou mais telefones do usuário formados por DDD e número
	* Um telefone de contato alternativo que não seja do usuário
	* Endereço formado por CEP, logradouro, complemento (que pode ou não existir), bairro, localidade e UF
	* Estado civil
	* Comprovante de renda
	* Uma ou mais contas bancárias
	* Sexo
	* Foto de perfil do usuário
2. Toda conta bancária deve possuir:
	* Número de conta único e exclusivo
	* Agência
	* Saldo
	* Histórico de transações
	* Cheque especial
3. Toda transação deve ficar armazenada (formando um histórico de cada usuário) e conter as seguintes informações:
	* Usuário que realizou a movimentação
	* Usuário que recebeu a movimentação
	* A data da movimentação
	* O valor que foi movimentado
	* O status da movimentação (permitida, bloqueada)

<a id="business-rules"></a>
## Regras de negócio

<a id="overdraft"></a>
### Cheque especial
1. Para pessoas com renda abaixo de 1500, o cheque especial deve ser nulo
2. Para pessoas com renda abaixo de 2500, o cheque especial deve ser de 35%
3. Para pessoas com renda a cima de 2500, o cheque especial deve ser de 50%

<a id="account-oppening"></a>
### Abertura de conta
1. Para que a abertura de conta seja permitida, é necessário que o usuário tenha seu CPF totalmente regularizado, ou seja, sem pendências no Serasa e afins
2. O usuário precisa ter no mínimo 18 anos para abrir uma conta bancária

<a id="validations"></a>
### Validações
1. A validação de usuário para login deve ser feita em duas etapas. As opções de validação são:
	* O usuário pode validar seu login com sua senha e com um e-mail enviado de forma automática com um código de segurança de 8 caracteres aleatórios
	* O usuário pode validar seu login com sua senha e uma imagem de perfil
	* Com sua senha e um SMS enviado para o número de telefone cadastrado com um código de segurança de 8 caracteres aleatórios
2. Toda senha precisa ter, no mínimo, 14 caracteres que contenham:
	* No mínimo uma letra maiúscula
	* No mínimo uma letra minúscula
	* No mínimo um caractere especial
	* No mínimo um dígito numérico
	* Não podem haver dígitos numéricos sequenciais, tais como 12 ou 45
3. Para criação de conta, é obrigatório que o usuário tire uma foto do seu rosto para futuras validações e maior segurança
4. Todas as transações efetuadas são instantaneamente debitadas, sem a opção, inicialmente, de movimentações no crédito e afins

<a id="data-model"></a>
# Modelo de dados

<a id="conceptual-model"></a>
## Modelo conceitual

<a id="logical-model"></a>
## Modelo lógico

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