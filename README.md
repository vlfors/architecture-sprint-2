# pymongo-api

## Как запустить

Запускаем mongodb и приложение

```shell
docker compose up -d
```

Заполняем mongodb данными

```shell
./scripts/mongo-init.sh
```

## Как проверить

### Если вы запускаете проект на локальной машине

Откройте в браузере http://localhost:8080

### Если вы запускаете проект на предоставленной виртуальной машине

Узнать белый ip виртуальной машины

```shell
curl --silent http://ifconfig.me
```

Откройте в браузере http://<ip виртуальной машины>:8080

## Доступные эндпоинты

Список доступных эндпоинтов, swagger http://<ip виртуальной машины>:8080/docs

# Реализация задач
### Шардирование [диаграмма](task1_mongo-sharding.drawio) [mongo-sharding](mongo-sharding)
### Репликация [диаграмма](task2_mongo-sharding-repl.drawio) [mongo-sharding-repl](mongo-sharding-repl)
### Кэширование [диаграмма](task3_sharding-repl-cache.drawio) [sharding-repl-cache](sharding-repl-cache)
### Service Discovery и балансировка с API Gateway [диаграмма](task4_api_gateway.drawio)
### CDN [диаграмма](task5_api_gateway_cdn.drawio)