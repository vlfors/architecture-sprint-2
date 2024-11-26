# Mongo Sharding Replication Project

## Описание
Проект реализует шардирование с репликами в MongoDB с использованием Docker Compose.

## Пререквизиты
- Docker
- Docker Compose

## Установка и запуск

### 1. Запуск MongoDB и приложения
```shell
docker-compose -p  mongo-sharding-repl up --build -d
```

> **Примечание:** После запуска происходит настройка среды в `init-shards` в течение 3-4 минут.

### 2. Проверка завершения настройки
Для проверки завершения настройки выполните:
```shell
docker logs -t mongo-sharding-repl_init-shards_1
```

Ожидайте сообщение `Done!` в логах, например:
```
2024-11-26T18:52:12.675828298Z Done!
```

### 3. Наполнение данными
Для наполнения данными запустите скрипт `mongo-init.sh`:
```shell
cd scripts/
chmod +x mongo-init.sh
./mongo-init.sh
```

## Эндпоинты проверки
- Подсчет : `http://{address}:8080/helloDoc/count`
- Пользователи: `http://{address}:8080/helloDoc/users/ly5`


