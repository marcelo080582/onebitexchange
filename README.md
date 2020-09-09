Aplicativo que converte o valor de uma moeda para outra qualquer.

Rails 5.2

ruby 2.5.1

Clone o projeto para sua máquina

git clone git@github.com:marcelo080582/exchange.git

Acesse a pasta do projeto
cd exchange

Rode:
docker-compose build

Crie o banco de dados e rode as migrations.
docker-compose run --rm app bundle exec rails db:create db:migrate

Suba o servidor
docker-compose up

Acesse no browser o endereço http://localhost:3000/
