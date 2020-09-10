Aplicativo que converte o valor de uma moeda para outra qualquer.

Rails 5.2

ruby 2.5.1

Clone o projeto para sua máquina:
git clone git@github.com:marcelo080582/exchange.git

Acesse a pasta do projeto:
cd exchange

Rode:
docker-compose build

Crie o banco de dados e rode as migrations:
docker-compose run --rm app bundle exec rails db:create db:migrate

Crie uma conta gratuita no site https://currencydatafeed.com. Vá em Api no menu lateral e copie o Api Access Token.

No projeto, delete o arquivo credentials.yml.enc:
rm credentials.yml.enc

Acesse o bash:
docker-compose run --rm app bash

Rode:
EDITOR=nano bundle exec rails credentials:edit

Adicione essas duas linhas no arquivo:
currency_api_key: <sua_api_key>
currency_api_url: https://currencydatafeed.com/api/data.php

Em currency_api_key adicione o Api Access token e salve o arquivo.
Ctrl + x -> Y -> ENTER

Instale o jquery:
docker-compose run --rm app bundle exec yarn add jquery

Instale o bootstrap:
docker-compose run --rm app bundle exec yarn add bootstrap

Suba o servidor
docker-compose up

Acesse no browser o endereço http://localhost:3000/
