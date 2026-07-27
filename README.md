# cryptosa-web

Публичный лендинг и APK-дистрибуция для **cryptosa** — Polygon DEX арбитраж
сканера для Android.

Этот репозиторий существует отдельно от приватного
[`cryptosa`](https://github.com/oddsouls/cryptosa), чтобы:
- позволить GitHub Pages работать (нужен публичный репо),
- не класть 75-МБ APK в git-историю основного проекта.

## Содержимое

- `index.html` — лендинг с кнопкой скачивания.
- `cryptosa-1.0.0-arm64-debug.apk` — собираемый APK (arm64-v8a, debug).

## GitHub Pages

Сайт публикуется автоматически из ветки `main` через GitHub Pages:
**https://oddsouls.github.io/cryptosa-web/**

## Обновление APK

```bash
# Из основного проекта cryptosa:
flutter build apk --debug --target-platform android-arm64
cp build/app/outputs/flutter-apk/app-debug.apk \
   /path/to/cryptosa-web/cryptosa-1.0.0-arm64-debug.apk
# обновить размер/версию в index.html при необходимости, закоммитить, запушить
```
