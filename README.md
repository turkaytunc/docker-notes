# docker-notes

```bash
docker start
docker run
docker pull
docker ps
docker ps -a
docker images
docker rm
docker rmi
docker inspect
```

## example

```bash

# -e -> environment variable, -d -> detach mode
docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=db_pass123 -d mysql

```

## example 2

```bash

docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo

```

## example 3

```bash

docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password -e ME_CONFIG_MONGODB_SERVER=mongodb --net mongo-network --name mongo-express mongo-express

```

## container logs

```bash
docker logs <container-id>
```

## access container and execute commands in it

```bash
docker exec -it <container-id>
```

## creating network

```bash

docker network <network-name>

```
