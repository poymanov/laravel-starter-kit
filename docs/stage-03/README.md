# Этап 3 - Основные настройки

В `config/app.php` поменять часовой пояс:

```
'timezone' => 'Europe/Moscow',
```

---

Добавить в `.env.example` строки (заменяя существующие):

```
DB_CONNECTION=pgsql
DB_HOST=db
DB_PORT=5432
DB_DATABASE=db
DB_USERNAME=db
DB_PASSWORD=db

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```
