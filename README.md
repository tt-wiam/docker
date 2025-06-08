# Тестовое задание WIAM

## Требования к ПО

- ОС: Linux, Debian ... / Windows 10, 11 c [WSL](https://learn.microsoft.com/ru-ru/windows/wsl/install)
- Docker [Linux](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04) / [Windows](https://docs.docker.com/desktop/setup/install/windows-install/)
- Docker
  Compose [Linux](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04) /
  Windows (Поставляется вместе с Docker Desktop)

## Установка

Клонировать репозиторий (в Windows клонировать в файловую систему WSL ```\\wsl.localhost\Ubuntu\path\to\...```)

```
git clone https://github.com/tt-wiam/docker.git
```

Копировать ```.env.default``` в ```.env```.

## Управление контейнерами

Запускать команды из корня приложения

```
cd path\to\project
```

### Запустить

Запустить в отладочном режиме

```
docker compose up
```

Запустить в фоновом режиме

```
docker compose up -d
```

Пересобрать образ

```
docker compose up -d --build
```

### Остановить

```
docker compose down
```

### Дополнительно

- [API Документация](API.md)
- SWAGGER http://localhost:8080/

