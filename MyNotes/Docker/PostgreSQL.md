## PostgreSQL

Запуск **PostgreSQL** с паролем

в **Windows Powershell**
```shell
docker run -d `
  --name my-postgres `
  -p 5432:5432 `
  -e POSTGRES_PASSWORD=mysecretpassword `
  postgres:alpine
```

> Если эта команда в Powershell не работает, то удалите из кода апострофы `

в **Git-Bash/Linux/WSL 2.0/Mac**
```shell
docker run -d \
  --name my-postgres \
  -p 5432:5432 \
  -e POSTGRES_PASSWORD=mysecretpassword \
  postgres:alpine
```

1. ![амам](./imgPostgreSQL/1.png)


Подключиться через `psql`
```shell
docker exec -it my-postgres psql -U postgres
```

2. ![амам](./imgPostgreSQL/2.png)


- Выполнить несколько демонстрационных команд, например:

Получить список баз данных:
```sql
\l
```
3. ![амам](./imgPostgreSQL/3.png)


Получить версию:
```sql
SELECT version();
```

4. ![амам](./imgPostgreSQL/4.png)

выйти из БД
```sql
exit
```
