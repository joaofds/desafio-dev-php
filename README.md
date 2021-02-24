#### Bem-vindo ao desafio

Estamos muito felizes que você tenha chegado nessa etapa do nosso processo seletivo, para essa fase, desejamos que você resolva um desafio.

O objetivo é criar uma API para uma aplicação já existente de cadastro de clientes.

#### Requisitos

- Criar endpoints da API

#### Requisitos bônus

Esses requisitos não são obrigatórios, mas serão levados em consideração como pontos extras no momento da avaliação.

- Ter uma boa cobertura de código
- Organizar estrutura do projeto utilizando padrões de projetos
- Criar um front-end para consumir a api de listagem.

#### Critérios de avaliação

- Organização do projeto: Avalia a estrutura do projeto, documentação e uso de controle de versão;
- Coerência: Avalia se os requisitos foram atendidos;
- Boas práticas: Avalia se o projeto segue boas práticas de desenvolvimento, incluindo segurança e otimização;

#### Processo de submissão

O desafio deve ser entregue pelo GitHub.

Qualquer dúvida em relação ao desafio, responderemos por e-mail.

Bom trabalho!


## Documentação
----

**Assembleia de Condomínio**
----

Aplicação para controlar cadastro de clientes.

Dados para cadastrar um cliente são:

Nome

email

telefone

#### Setup

Utilizar a linguagem PHP com framework ou sem framework.

**API**
----

`METHOD` | `URL` | `PARAMS`

* **URL**

  `/api/v1`

----

* **Get All Clientes**

    `GET` | `/clientes`
    example: curl --location --request GET 'http://localhost:8000/api/v1/clientes'
    
* **Create Cliente**

  `POST` | `/clientes` 
  
  example:
  curl --location --request POST 'http://localhost:8000/api/v1/clientes' \
  --header 'Content-Type: application/json' \
  --data-raw '{
    "nome":"Uzer",
    "email": "uzer@uzer.com",
    "telefone": 6284169052
  }'
  
* **Show Clientes**

  `GET` | `/clientes/:id`
  example: 
  curl --location --request GET 'http://localhost:8000/api/v1/clientes/1'
  
* **Update Cliente**

  `PATCH` | `/clientes/:id`

  example: 
  curl --location --request PUT 'http://localhost:8000/api/v1/clientes/2' \
--header 'Content-Type: application/json' \
--data-raw '{
	"nome":"Uzer",
  "email": "uzer@uzer.com",
   "telefone": 6284169052
}'

