# Этап 6 - Настройка Laravel Pint

Скопировать `pint.json` в корень проекта.

Добавить в `composer.json`, в `scripts`:

```
"pint": "vendor/bin/pint --test",
"pint-fix": "vendor/bin/pint",
```
