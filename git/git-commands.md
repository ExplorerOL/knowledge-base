# Настройка git
## Файлы настроек
- Системный уровень (`--system`)
Настройки применяются ко **всем пользователям** системы.
    Linux / macOS: `/etc/gitconfig`   
    Windows: `C:\Program Files\Git\etc\gitconfig`
- Глобальный уровень (`--global`)
Настройки применяются **только к текущему пользователю**.
    Linux / macOS: `~/.gitconfig`   или `~/.config/git/config`\
    Windows: `C:\Users<ИМЯ_ПОЛЬЗОВАТЕЛЯ>.gitconfig`
- Локальный уровень (`--local`)
Настройки применяются **только к конкретному репозиторию**. Файл находится находится внутри репозитория `.git/config`

Если один и тот же параметр задан на нескольких уровнях, Git применяет их в следующем порядке (от низкого к высокому приоритету):

system → global → local


### Просмотр текущей конфигурации
```
git config --list
```
### Просмотр источника настройки
```
git config --show-origin user.name
```
### Задание имени пользователя и почты
Глобально
```
git config --global user.name "<username>"
git config --global user.email "<email>"
```

Для репозитория
```
git config user.name "<username>"
git config user.email "<email>"
```