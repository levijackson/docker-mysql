# Docker MySQL
An easy way to set up a MySQL install to do some testing.

## Setup
1. Start the containers `docker-compose up -d`
2. Log into PHPMyAdmin http://localhost:8080
  - use the credentials from `.env` (`MYSQL_USER` and `MYSQL_PASSWORD`)

If you'd like to customize the username/password for mysql, set the environment variables.
```
MYSQL_ROOT_PASSWORD=<value> MYSQL_DATABASE=<value> MYSQL_USER=<value> MYSQL_PASSWORD=<value> docker-compose up -d
```

## Shutting down
`docker-compose down` will turn off the containers, but the volumes will persist. If you want to start fresh and *delete* the database, run `docker-compose down --volumes` and it will delete the volumes.