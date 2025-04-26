1) Запустить с помощью docker compose Redis + Redis Commander (GUI для Redis)
2) Запустить с помощью docker compose Minio
3) Запустить с помощью docker compose приложение https://github.com/AnastasiyaGapochkina01/go-http-db/tree/main
- добавить к сервису БД healthcheck
- добавить сервис migrator
```
migrations:
  image: postgres:15
  restart: on-failure
  environment:
    PGPASSWORD: postgres
  volumes:
     - ./migrations:/migrations
  command: >
    sh -c "while ! pg_isready -h db -U postgres; do sleep 1; done
      && psql -h db -U postgres -d app_db -f /migrations/001_init.sql"
```
- проверить командой ```curl http://localhost:8080/hello```
