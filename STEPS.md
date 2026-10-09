# Что сделать вручную (пп. 6, 11)

Эти шаги требуют вашего аккаунта GitHub и второго студента, поэтому выполнить их за вас нельзя.

## 1. Создать репозиторий и загрузить проект (п. 6)

1. На GitHub нажмите **New repository**, назовите его `style-guide-project`, оставьте пустым (без README и `.gitignore`).
2. В каталоге проекта выполните:

   ```bash
   git init -b main
   git add .
   git commit -m "feat: initial style guide structure"
   git remote add origin https://github.com/YOUR-USERNAME/style-guide-project.git
   git push -u origin main
   ```

3. В `mkdocs.yml` замените `YOUR-USERNAME` на ваш логин GitHub (`site_url` и `repo_url`).

## 2. Включить публикацию (п. 10)

1. В репозитории откройте **Settings → Pages**.
2. В поле **Source** выберите **Deploy from a branch**, ветку `gh-pages`, каталог `/ (root)`. Ветка `gh-pages` появится после первого успешного запуска CI на `main`.
3. Откройте **Settings → Actions → General → Workflow permissions** и включите **Read and write permissions**.

## 3. Ветка, раздел, Pull Request (п. 11)

Раздел «Доступность текста» уже написан и лежит в `docs/accessibility.md`. Чтобы пройти процесс как в задании, не добавляйте его в `main` сразу:

1. Перед первым коммитом удалите из `mkdocs.yml` строку навигации `- Доступность текста: accessibility.md` и перенесите файл `docs/accessibility.md` во временное место.
2. После первого коммита и пуша создайте ветку:

   ```bash
   git checkout -b docs/accessibility-rules
   ```

3. Верните `docs/accessibility.md` и строку навигации в `mkdocs.yml`.
4. Закоммитьте:

   ```bash
   git add docs/accessibility.md mkdocs.yml
   git commit -m "docs(accessibility): add text accessibility rules"
   git push -u origin docs/accessibility-rules
   ```

5. На GitHub нажмите **Compare & pull request** и создайте Pull Request в `main`.
6. Отправьте ссылку на PR другому студенту и получите ссылку на его PR.
7. Оставьте минимум три комментария к его PR (замечание, предложение, вопрос).
8. Исправьте свои замечания новым коммитом, например `fix(accessibility): clarify alt text rule`, и сделайте `git push`.
9. После одобрения нажмите **Merge pull request**.
10. Откройте вкладку **Actions** и убедитесь, что запуск на `main` завершился успехом, а сайт обновился по адресу `https://YOUR-USERNAME.github.io/style-guide-project/`.
