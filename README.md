# pgadmin4-dc
Run pgadmin4 locally using docker-compose. Uses the docker container, [dpage/pgadmin4](https://hub.docker.com/r/dpage/pgadmin4).

## Why?
To make life easier.

## Use
```
docker network create pgadmin
docker-compose up
```

## Example Complimentary Web Service Config
```
services:
  web:
    ...
    networks:
      backend:
        aliases:
          - my-web-app

  db:
    ...
    networks:
      backend:
        aliases:
         - my-web-app-db
      pgadmin:
        aliases:
          - my-web-app-db

networks:
  backend:
  pgadmin:
    external: true

```

## pgAdmin

Please show love to the team that built pgAdmin: https://www.pgadmin.org/
