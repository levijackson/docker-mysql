# Docker MySQL
An easy way to set up a MySQL install to do some testing.

## Setup
1. Copy `.env.example` to `.env` and fill it out.
If you're running it in development, I found this to do the job quickly
```
MYSQL_ROOT_PASSWORD=password
MYSQL_DATABASE=dev-db
MYSQL_USER=dev-user
MYSQL_PASSWORD=password
# this allows any domain to connect. Useful if you're testing from something other than localhost
MYSQL_ROOT_HOST=%
```
2. Start the containers `docker-compose up -d`
3. Log into PHPMyAdmin http://localhost:8080
  - use the credentials from `.env` (`MYSQL_USER` and `MYSQL_PASSWORD`)

If you'd like to customize the username/password for mysql, copy `.env.example` => `.env` and fill in the values.

`MYSQL_ROOT_HOST=%` can be used if you're working in a dev environment to get access quickly.

## Shutting down
`docker-compose down` will turn off the containers, but the volumes will persist. If you want to start fresh and *delete* the database, run `docker-compose down --volumes` and it will delete the volumes.