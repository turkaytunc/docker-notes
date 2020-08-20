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
