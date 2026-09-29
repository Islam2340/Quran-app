# Как получить APK

## Вариант 1 — Android Studio

1. Распакуйте архив проекта.
2. Установите Android Studio на компьютер.
3. Откройте в Android Studio папку `Коран_APK_Project`.
4. Дождитесь завершения синхронизации Gradle.
5. Выберите **Build → Generate App Bundles or APKs → Generate APKs**.
6. Готовый файл будет находиться примерно здесь:
   `app/build/outputs/apk/debug/app-debug.apk`
7. Передайте APK на телефон и установите его.

## Вариант 2 — без установки Android Studio

В проект уже добавлен GitHub Actions workflow `.github/workflows/build-apk.yml`.

1. Создайте новый репозиторий на GitHub.
2. Загрузите туда содержимое папки проекта.
3. Откройте вкладку **Actions**.
4. Выберите **Build Quran APK**.
5. Нажмите **Run workflow**.
6. После завершения откройте выполненный workflow и скачайте artifact **Quran-debug-apk**.
7. Внутри будет `app-debug.apk`.

Это debug-версия для установки на Android. Для публикации в Google Play потребуется отдельная release-сборка с подписью.
