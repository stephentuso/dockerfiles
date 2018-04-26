# mattes-migrate-compose

For running [migrate](https://github.com/mattes/migrate) in docker-compose - includes `bash` and [wait-for-it.sh](https.://github.com/vishnubob/wait-for-it) available as `wait-for-it`.

For example:

```
services:
  postgres:
    image: "postgres:9.6.1"
    ports:
      - "5432:5432"
    environment:
      POSTGRES_USER: "test"
      POSTGRES_PASSWORD: "test"
      POSTGRES_DB: "test"

  schema:
    image: "stephentuso/mattes-migrate-compose"
    command: >
      wait-for-it postgres:5432 --
      migrate -source file:///migrations
      -database postgres://test:test@postgres:5432/test?sslmode=disable up
    volumes:
      - "./migrations:/migrations"
    depends_on:
      - postgres
```