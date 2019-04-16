# Docker sample

## version
- ruby: 2.6.1
- rails: 5.2.2.1
- mysql: 5.7
- mysql2: 0.4.10

## docker files
- Dockerfile: /docker/development
- docker-compose.yml: /
- modified database.yml

```database.yml
username: <%= ENV.fetch("MYSQL_USERNAME", "root") %>
password: <%= ENV.fetch("MYSQL_PASSWORD", "root") %>
host: <%= ENV.fetch("MYSQL_HOST", "database") %>
```
> host: localhost  
username: root  
password: root  
port: 4306
## docker command
- build: `$ docker-compose build`
- start app: `$ docker-compose up`
- bundle install: `docker-compose run --rm app bundle install`
