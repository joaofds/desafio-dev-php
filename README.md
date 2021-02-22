#### Bem-vindo ao desafio

Estamos muito felizes que você tenha chegado nessa etapa do nosso processo seletivo, para essa fase, desejamos que você resolva um desafio.

O objetivo é criar uma API para uma aplicação já existente de cadastro de assembleias.

#### Requisitos

- Criar endpoints da API

#### Requisitos bônus

Esses requisitos não são obrigatórios, mas serão levados em consideração como pontos extras no momento da avaliação.

- Ter uma boa cobertura de código
- Organizar estrutura do projeto utilizando padrões de projetos
- Criar um front-end para consumir a api.

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

**Agenda Mail**
----

Aplicação para troca de mensagens entre usuários.

Possui usuario master, que pode visualizar todas as mensangens, inclusive arquivadas.

Usuario Master:

email: master@email.com

password: 123456

#### Setup

```
bundle install
bundle exec rails db:setup
```

**API**
----

`METHOD` | `URL` | `PARAMS`

* **URL**

  `/api/v1`

* **Required**

  `Authorization=[string]` user's token send in header request. Get your token in profile page

  It's a constant value for master token

----

* **Messages**

    `GET` | `/messages`

    example: `curl '/api/v1/messages' -H 'Authorization: xxx'`

* **Create Message**

  `POST` | `/messages` | `message[title]=string&message[content]=string`

  example: `curl -X POST '/api/v1/messages' -H 'Authorization: xxx' -d 'message[receiver_email]=matheus@email.com&message[title]=APITEST&message[content]=CONTEUDO'`

* **Sent**

    `GET` | `/messages/sent`

    example: `curl '/api/v1/messages/sent' -H 'Authorization: xxx'`

* **Show Message**

  `GET` | `/messages/:id`

  example: `curl '/api/v1/messages/1' -H 'Authorization: xxx'`

  OR `curl '/api/v1/messages/1' -H 'Authorization: xxx'`

* **Show Profile**

`GET` | `/profile`

example: `curl '/api/v1/profile' -H 'Authorization: xxx'`

* **Update Profile**

  `PATCH` | `/profile` | `user[name]=string&user[email]=string&user[password]=string&user[password_confirmation]=string`

  example: `curl -g -X PATCH '/api/v1/profile?user[name]=Mateus' -H 'Authorization: xxx'`

