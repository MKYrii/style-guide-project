# Руководство по стилю документации

Стайлгайд для документации программного проекта, оформленный по методологии Docs as Code: Markdown, MkDocs, линтинг, CI/CD.

## Локальная сборка

```bash
pip install -r requirements.txt
mkdocs serve
```

Сайт откроется на `http://127.0.0.1:8000`.

## Структура репозитория

| Путь | Назначение |
|---|---|
| `docs/` | Разделы руководства |
| `mkdocs.yml` | Настройки сайта и навигация |
| `.markdownlint.yml` | Правила линтера Markdown |
| `.github/workflows/ci.yml` | Проверка и публикация |
| `CONTRIBUTING.md` | Как вносить изменения |

Подробности о внесении изменений — в [CONTRIBUTING.md](CONTRIBUTING.md).
