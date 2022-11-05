# Этап 10 - Настройка тестирования

Добавить в `config/database.php`:

```php
'pgsql-test' => [
    'driver' => 'pgsql',
    'url' => env('DATABASE_URL'),
    'host' => env('DB_HOST', '127.0.0.1'),
    'port' => env('DB_PORT', '5432'),
    'database' => env('DB_DATABASE_TEST', 'forge'),
    'username' => env('DB_USERNAME', 'forge'),
    'password' => env('DB_PASSWORD', ''),
    'charset' => 'utf8',
    'prefix' => '',
    'prefix_indexes' => true,
    'search_path' => 'public',
    'sslmode' => 'prefer',
],
```

Выполнить консольную команду, чтобы зайти внутрь контейнера с php:

```
make backend-shell
```

Выполнить консольную команду:

```
composer require --dev pestphp/pest pestphp/pest-plugin-faker pestphp/pest-plugin-laravel
```

Согласиться с вопросом (если он появится):

```
Do you trust "pestphp/pest-plugin" to execute code and wish to enable it now? (writes "allow-plugins" to composer.json) [y,n,d,?] 
```

Нажать `y`.

Выполнить:

```
php artisan pest:install
```

Скопировать директории - `tests/Feature` и `test/Unit`.

Добавить в `composer.json`, в `scripts`:

```
"test": "php artisan test",
"test-coverage": "XDEBUG_MODE=coverage php artisan test --coverage",
```

Заменить строки в `phpunit.xml`:

```
<env name="DB_CONNECTION" value="pgsql-test"/>
<env name="DB_DATABASE_TEST" value="db-test"/>
```

Там же, в блок добавить:
```
<report>
    <html outputDirectory="tests/Coverage/html"/>
</report>
```
