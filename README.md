# Docker

#### Сбилдить образ
```
docker build . --file Dockerfile --tag image-tag
```

Dockerfile используется по умолчанию, указывать его нужно только если используется другое имя файла

#### Запустить образ

```
docker run image_id/image_tag
```

#### Открыть консоль контейнера

```
docker exec -it container_id /bin/sh
```

#### Вывести список образов

```
docker images
docker image -ls 
```

#### Вывести список запущенных контейнеров

```
docker ps
docker ps -a  # все, включая остановленные
```

#### Удаление

+ Удалить image:

```
docker rmi image_id
```

+ Удалить container:

```
docker rm container_id
```

+ Удалить все остановленные контейнеры, networks, образы (которые не связаны хотя бы с одним контейнером)

```
docker system prune -a
```