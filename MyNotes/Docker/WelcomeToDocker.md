## Welcome to Docker

Для выполнения задания создайте в репозитории отдельную папку `Docker`, в ней папку `img` и папку `WelcomeToDocker` и в ней файл `README.md`.

Выполните все этапы работы с проектом по примеру с [Nginx](/content/Docker/ImageLibrary/Nginx.md)

> Перед созданием проекта убедитесь, что порт `8088` не занят другим приложением!

Проверить порт `8088` для **Linux/Mac/WSL**:
```shell
# Проверьте, занят ли порт
netstat -tuln | grep :8088
```
> Если эта команда ничего не возвращает, то порт свободен

Проверить порт `8088` для **Windows**:
```shell
netstat -aon | findstr :8088
```

Загрузить образ и запустить контейнера
```shell
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```

[Открыть http://localhost:8088 в браузере](http://localhost:8088)

1. ![амам](./imgWelcomeToDocker/7.png)

2. ![амам](./imgWelcomeToDocker/2.png)

Зайти в контейнер
```shell
docker exec -it welcome-to-docker /bin/sh
```

3. ![амам](./imgWelcomeToDocker/1.png)

Повыполнять разные команды:

Показать ин-фу по ОС
```shell
uname -a
```

4. ![амам](./imgWelcomeToDocker/9.png)

Диспетчер ресурсов
```shell
top
```

5. ![амам](./imgWelcomeToDocker/3.png)

Обновить источники приложений
```shell
apk update && apk upgrade
```

5. ![амам](./imgWelcomeToDocker/4.png)

Установить приложение
```shell
apk add fastfetch
```

6. ![амам](./imgWelcomeToDocker/5.png)

Запустить приложение
```shell
fastfetch
```

7. ![амам](./imgWelcomeToDocker/6.png)

