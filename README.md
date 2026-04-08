# Helpers

Репозиторий с конфигурациями и настройками для различных инструментов разработки.

## 📂 Структура

### VSCode (`vscode/`)

Конфигурационные файлы для Visual Studio Code:

- **`settings.json`** — основные настройки редактора (форматирование, отступы, расширения)
- **`launch.json`** — конфигурации для запуска и отладки проектов
- **`extensions.json`** — рекомендуемые расширения для проекта

### Git Bash (`bash/`)

Темы и конфигурации для Git Bash терминала:

- **`.minttyrc`** — конфигурация при тёмной теме
- **`.minttyrc (light)`** — конфигурация при светлой теме

### Git (`git/`)

Глобальные настройки Git:

- **`.gitconfig`** — конфигурация пользователя Git (имя, email, алиасы)
- **`.gitignore_global`** — глобальный файл исключений для всех репозиториев

### GitHub Rulesets (`rulesets/`)

Правила защиты для GitHub:

- **`Branch Protection.json`** — правила защиты веток
- **`Tag Protection.json`** — правила защиты тегов

## 🚀 Использование

### Установка VSCode конфигурации

Скопируйте файлы из папки `vscode/` в ваш пользовательский каталог VS Code:

- Windows: `%APPDATA%\Code\User\`
- macOS: `~/Library/Application Support/Code/User/`
- Linux: `~/.config/Code/User/`

### Установка Git конфигурации

```bash
# Копируем глобальный gitconfig
cp git/.gitconfig ~/.gitconfig

# Копируем глобальный gitignore
cp git/.gitignore_global ~/.gitignore_global

# Подключаем gitignore в конфигурацию Git
git config --global core.excludesfile ~/.gitignore_global
```

### Установка Git Bash темы

Скопируйте нужный файл `.minttyrc` в домашний каталог:

```bash
cp bash/.minttyrc ~/ # для тёмной темы
cp bash/.minttyrc\ \(light\) ~/.minttyrc # для светлой темы
```

### Применение GitHub Rulesets

1. Перейдите в ваш репозиторий на GitHub
2. Settings → Rules → New branch ruleset / New tag ruleset
3. Загрузите соответствующий JSON файл из папки `rulesets/`

## 📝 Примечания

- Все конфигурации можно кастомизировать под ваши нужды
- При обновлении системы рекомендуется проверить совместимость конфигов
- Убедитесь, что у вас установлены все необходимые расширения для VSCode
