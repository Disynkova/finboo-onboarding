# Finboo: гайд для фрилансеров

Статическая страница с пошаговой инструкцией для новых фрилансеров: регистрация, профиль (KYC), верификация, способ вывода, договор, первый счёт.

## Состав

- `index.html` — вся страница: разметка, стили и скрипты в одном файле.
- `img/` — скриншоты интерфейса (WebP, 1600×849).
- `.nojekyll` — отключает обработку Jekyll на GitHub Pages.

Сборка не нужна. Внешние зависимости: только шрифты Google Fonts (Manrope, Onest).

## Публикация на субдомене

### Вариант A. GitHub Pages

1. Settings → Pages → Build and deployment → Source: **Deploy from a branch**, ветка `main`, папка `/ (root)`.
2. В поле **Custom domain** указать субдомен, например `help.finboo.io`. GitHub сам добавит в репозиторий файл `CNAME`.
3. В DNS домена добавить запись: `CNAME  help  →  disynkova.github.io`.
4. После проверки DNS включить **Enforce HTTPS**.

### Вариант B. Свой хостинг

Подключить репозиторий к Vercel, Netlify или Cloudflare Pages (framework: none, build command пустой, output directory `/`) или забирать файлы на свой сервер. Корневой файл — `index.html`.

## Обновления

Изменения вносятся коммитами в `main`. Хостинг пересобирает сайт автоматически после каждого пуша.

Якоря разделов для ссылок из поддержки: `#start`, `#accept`, `#kyc`, `#verify`, `#payout`, `#contract`, `#invited-done`, `#invoice`, `#after`, `#faq`.
