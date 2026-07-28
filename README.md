# Сайт-визитка Sergei Kolesnikov

Статический сайт. Вся вёрстка — в `index.html`, все тексты и картинки — в `content/site.json`.
Сборка не нужна: GitHub Pages отдаёт файлы как есть.

```
index.html            вёрстка и логика
content/site.json     тексты (EN / ES) и настройки контактов
assets/               фото, логотипы, аватар
.pages.yml            описание полей для админки Pages CMS
.nojekyll             отключает обработку Jekyll
```

## Обновление сайта на GitHub

Аккаунт переименован в **serkolesnikov**, поэтому репозиторий тоже надо переименовать:
Settings → General → Repository name → **serkolesnikov.github.io** → Rename.
После этого адрес сайта: **https://serkolesnikov.github.io**

Затем загрузите файлы из этой папки поверх существующих:
Add file → Upload files → перетащить `index.html`, папки `content` и `assets`, файл `.pages.yml` → Commit changes.

## Админка

app.pagescms.org → вход через GitHub → репозиторий `serkolesnikov.github.io` → раздел «Сайт».
Правки уходят коммитом, сайт обновляется за 1–2 минуты.

## Форма заявок

Сейчас кнопка открывает почтовый клиент. Чтобы заявки приходили письмом с сайта:
formspree.io → создать форму → скопировать endpoint вида `https://formspree.io/f/xxxxxxx` →
вставить в админке в поле «Formspree endpoint».

## Локальная проверка

Открывать `index.html` двойным щелчком нельзя — браузер не даст прочитать `content/site.json`.
Запустите `python3 -m http.server` в этой папке и откройте http://localhost:8000
