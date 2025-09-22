# gost-env

Этот репозиторий содержит удобный набор скриптов для работы с окружением Gost.

## Prerequisites

- Docker
- direnv (optional)

## Quick Start

```bash
# клонируем репозиторий
git clone https://github.com/kxddry/gost-env.git
cd gost-env

# создаём .bin/.env, наполняем его данными
touch .bin/.env
echo "GIT_USERNAME=your_username" >> .bin/.env
echo "GIT_PASSWORD=your_password" >> .bin/.env
echo "GIT_NAME=your_name" >> .bin/.env
echo "WOODPECKER_AGENT_SECRET=base64_encoded_secret" >> .bin/.env

# разрешаем direnv
direnv allow
```

## Usage

- После захода в нужную директорию, выполните `start` для запуска контейнера для работы с git.
- Для запуска агента woodpecker, выполните `agent`.
- Для запуска агента woodpecker в фоне, выполните `agentd`.
- Для остановки агента woodpecker, выполните `stop-agent`.
- Для остановки контейнера для работы с git, выполните `stop`.

### Woodpecker Agent

Бинарник woodpecker-agent и woodpecker-cli нужно разместить в директории .bin для запуска агента.

