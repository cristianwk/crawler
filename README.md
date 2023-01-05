## Autor

Cristian Marques
05/01/2023

## Desafio

Encontrar “a resposta”, utilizando um crawler.
“A resposta" se encontra atrás do clique de um botão, aqui: http://applicant-test.us-east-1.elasticbeanstalk.com/

Ter um crawler que emita requisições e leia as respostas, em baixo nível
(sem emuladores de browser, como puppeteer, selenium, phantomjs, jsdom, etc).
Esse crawler deve ser capaz de ler “a resposta" produzida e escrevê-la na tela.

### Requirements

-   Docker
-   Docker Compose
-   Laravel

### Setup

Criar um ".env" baseado no ".env.example"

Iniciar contêineres desanexados do terminal em execução:
docker-compose up -d

RUN useradd -G www-data,root,sudo,chrome -u 1000 -d /home/

em seguida, executar o composer dentro do container do docker
docker-compose exec app composer install

### Run Teste

para executar o teste dentro do container
docker-compose exec app php ./vendor/bin/phpunit

app:

-   http://localhost:8080/
