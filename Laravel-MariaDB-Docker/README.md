# Laravel-MySQL-Docker README

This project contains the required files to run Laravel 9.x in Docker with PHP 8.2, debugging
and persistent storage for MySQL 8.

## How to
1. Copy the docker folder into the root (top level) of an existing Laravel 9.x project
2. Within the directory run the docker compose command, changing **-p <project-name>** below to the name you would like to use.

For example from:

`docker compose p <project-name> -f "docker\docker-compose.yml" up -d --build`

To:

`docker compose p my-amazing-app -f "docker\docker-compose.yml" up -d --build`

## MySQL credentials
Modify lines 31 to 34 in **docker-compose.yml** to the credentials you would like to use.

## PhpStorm notes
By default, PhpStorm tries to listen on port 9000, then 9003 for xdebug requests.
However, nginx/php-fpm already uses this port.
In settings > PHP > Debug ensure that debug port is set to only 9003 

## Optional - Modify files
1. To remove persistent storage, remove lines 28 and 29 from **docker-compose.yml**
2. To change xdebug config **Dockerfile** (not recommended)

