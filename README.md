# pgadmin4-dc
Run pgadmin4 locally using docker-compose. Uses the docker container, [dpage/pgadmin4](https://hub.docker.com/r/dpage/pgadmin4).

## Why?
To make life easier.

## Use
```
docker-compose up
```

## Example Complimentary Web Service Config
```
version: "3.7"

services:
  web:
    ...
    networks:
      local-dev:
        aliases:
          - my-web-app

  db:
    ...
    networks:
      local-dev:
        aliases:
          - my-web-app-db

networks:
  local-dev:
    external:
      name: dev

```

## pgAdmin

Please show love to the team that built pgAdmin: https://www.pgadmin.org/
