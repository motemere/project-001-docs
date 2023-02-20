# Описание сервисов

## Сервисы

### Телеграм-бот

#### Описание

Телеграм-бот для получения информации о состоянии системы и управления ею.

#### Конфигурация

Пример yaml-конфигурации:

```yaml
# configurations/telegram-bot.yaml
telegram_bot:
  token: !secret telegram_bot_token
  allowed_chat_ids:
    - !secret telegram_bot_chat_id
```

### Сервис состояния системы

#### Описание

Стейтфул-сервис, который хранит в себе состояние системы.

#### Конфигурация

Пример yaml-конфигурации:

```yaml
# configurations/state.yaml
config:
  bot_url: !secret telegram_bot_url
  state: 'off'
  last_state: 'on'
```

### Сервис логгирования состояния системы

#### Описание

Сервис, который логгирует состояние системы в файл.

#### Конфигурация

Пример yaml-конфигурации:

```yaml
# configurations/logger.yaml
logger:
  filename: !secret logger_filename
  level: !secret logger_level
```
