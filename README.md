# docker-kanboard-postgres

Docker Compose with Kanboard and Postgres.

[Kanboard](https://kanboard.net) is a free and open sourced, self-hosted Kanban board: https://github.com/kanboard/kanboard

This repository contains a docker-compose.yml to run Kanboard with PostgreSQL and data has been encapulating into a directory for simple backup.

## Prerequisite

* installed docker and docker-compose

* (fork and) clone this repo

* ```chmod 777 data/ plugins/```

## Start and Stop

    docker-compose up -d

    docker-compose down

## Directories:

* *db:* contains PostgreSQL database

* *plugins:* Kanboard plugins downloaded here

* *data:* Kanboard data directory, contains config file

## Configuration:

* *.env*: contains version numbers, and *database password: do not afraid to change it!*

* *set an exact version number for kanboard:* replace kanboard_version=latest

Check config.php and postgres.sql files: it must comes from Kanboard v{kanboard_version}

* *data/config.php:*: standard [Kanboard configuration file](https://kanboard.net/documentation/config) prepared to using instantly; *DB_PASSWORD is the database password: do not afraid to change it!* https://github.com/kanboard/kanboard/blob/master/config.default.php

* *Database preparation:* *postgres.sql* file is Kanboard [app/Schema/Sql/postgres.sql](https://kanboard.net/documentation/postgresql-configuration) and https://github.com/kanboard/kanboard/tree/master/app/Schema/Sql

## Backup:

* Save *data* and *plugins* directory.

* PostgreSQL dump for database (*db* directory)
