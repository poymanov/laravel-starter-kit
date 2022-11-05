# Этап 7 - Установка Larastan

Выполнить консольную команду, чтобы зайти внутрь контейнера с php:

```
make backend-shell
```

Выполнить консольную команду:

```
composer require --dev nunomaduro/larastan
```

Добавить в composer.json, в `scripts`:

```
"phpstan": "phpstan analyse",
```

Скопировать `phpstan.neon.dist` в корень проекта.
