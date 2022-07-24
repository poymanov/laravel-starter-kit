# Этап 1 - Docker

Для запуска приложения требуется **Docker** и **Docker Compose**.

Директорию `docker` и файлы `Makefile`, `docker-compose.yml` нужно скопировать полностью.

В `docker-compose.yml`, для контейнера `php-fpm` поменять на своё значение переменную окружения:

```
environment:
    PHP_IDE_CONFIG: serverName=your-app
```
