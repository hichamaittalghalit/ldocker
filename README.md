# L-Docker

1 - Clone "chamhi-docker" inside your PHP project:

    git clone https://github.com/hichamaittalghalit/ldocker docker


2 - Enter the "docker" folder and rename env-example to .env.

    cd docker && cp .env.example .env

3 - Stop `apache2` service if it runs on your server Linux: (same for `nginx` service):
    
    systemctl stop apache2
    
OR uninstall it
    
    apt remove --purge apache2 -y

## NOTICE

Change your `mysql` database credentials in `.env` file:

    MYSQL_PASSWORD=xxxxxx
    MYSQL_ROOT_PASSWORD=xxxxxx

## SCRIPTS

1 - Run containers

    sh up.sh

2 - Stop containers

    sh stop.sh

3 - Enter the Workspace container

    sh run.sh
    
4 - Stop & Run Containers, & Enter To Workspace Containers    

    sh reload.sh
