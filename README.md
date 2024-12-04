based on https://github.com/laradock/laradock

# L-Docker

1 - Stop `apache2` service if it runs on your server Linux: (same for `nginx` service)

    systemctl stop apache2

OR uninstall it

    apt remove --purge apache2 -y

2 - Clone `ldocker`

    git clone https://github.com/hichamaittalghalit/ldocker docker


3 - Enter the "docker" folder and rename env-example to .env.

    cd docker && cp .env.example .env

4 - Change your `mysql` database credentials in `.env` file

    MYSQL_PASSWORD=xxxxxx
    MYSQL_ROOT_PASSWORD=xxxxxx

5 - GO FOR IT :P

    docker compose build redis mysql php-fpm workspace php-worker nginx

## CMD

1 - Run containers

    docker compose down redis mysql php-fpm workspace php-worker nginx

2 - Stop containers

    sh stop.sh

3 - Enter the Workspace container

    docker compose exec workspace bash

