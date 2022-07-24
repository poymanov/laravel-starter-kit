# Этап 10 - Установка PHP Pest

Выполнить консольную команду, чтобы зайти внутрь контейнера с php:

```
make backend-shell
```

Выполнить консольную команду:

```
composer require --dev pestphp/pest pestphp/pest-plugin-faker pestphp/pest-plugin-laravel
```

Согласиться с вопросом:

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
"test": "vendor/bin/pest",
```
