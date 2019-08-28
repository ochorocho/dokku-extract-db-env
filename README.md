# Dokku extract db to env vars plugin

The plugin aims to split the `DATABASE_URL` (DSN) into single variables.

## Install

```
dokku plugin:install https://github.com/ochorocho/dokku-extract-db-env.git extract-db-env
```

## What it does

Adds the file `/app/.profile.d/extract_db_env.sh` with some `export` variables.
This file is used to export EVN VARs

The file will look like this:

```
export DATABASE_TYPE='mysql'
export DATABASE_USER='mariadb'
export DATABASE_PASSWORD='PASSWORD'
export DATABASE_HOST='dokku-mariadb-app-name-database'
export DATABASE_PORT='3306'
export DATABASE_NAME='app_name_database'
```
