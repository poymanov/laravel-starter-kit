# Этап 11 - Установка Laravel Telescope

Выполнить консольную команду, чтобы зайти внутрь контейнера с php:

```
make backend-shell
```

Выполнить консольную команду:

```
composer require laravel/telescope
```

Добавить данные для отдельной БД логирования в `config/database`:

```
'pgsql-telescope' => [
    'driver' => 'pgsql',
    'url' => env('DATABASE_URL'),
    'host' => env('DB_HOST', '127.0.0.1'),
    'port' => env('DB_PORT', '5432'),
    'database' => env('DB_DATABASE_TELESCOPE', 'forge'),
    'username' => env('DB_USERNAME', 'forge'),
    'password' => env('DB_PASSWORD', ''),
    'charset' => 'utf8',
    'prefix' => '',
    'prefix_indexes' => true,
    'search_path' => 'public',
    'sslmode' => 'prefer',
],
```

И выполнить миграции:

```
php artisan migrate
```

Laravel Telescope доступен по адресу - http://localhost:8080/telescope
