# Этап 9 - Установка Laravel IDE Helper

Выполнить консольную команду, чтобы зайти внутрь контейнера с php:

```
make backend-shell
```

Выполнить консольную команду:

```
composer require --dev barryvdh/laravel-ide-helper
```

Добавить в composer.json, в `scripts`:

```
"ide-helper-generate": "php artisan ide-helper:generate",
"ide-helper-models": "php artisan ide-helper:models -M",
"ide-helper-meta": "php artisan ide-helper:meta",
```

Во время разработки после добавления новых моделей необходимо выполнять команду:

```
make backend-ide-helper
```
