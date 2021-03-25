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
# -e environment variables -p hostport:dockerport
docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo

```

## example 3

```bash
# --net network
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password -e ME_CONFIG_MONGODB_SERVER=mongodb --net mongo-network --name mongo-express mongo-express

```

## example 4

```bash
#creating network
docker create network wp-mysql-network --driver bridge --subnet 182.18.0.1/24 --gateway 182.18.0.1

```

## example 5

```bash

docke run -d -p 4000:4000 --env-file ./.env --name api-app api-image

```

## react-application dockerfile example

```bash
FROM mhart/alpine-node:latest as react-build
WORKDIR /usr/app/react
COPY ["package.json", "./"]
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=react-build /usr/app/react/build /usr/share/nginx/html
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
