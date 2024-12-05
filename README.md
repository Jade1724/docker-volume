# Docker Volume Practice

## Docker commands

Build image

```
docker build -t feedback-node .
```

Create and run the container

```
docker run -p 3000:80 -d --name feedback-app --rm feedback-node
```

Stop the container

```
docker stop feedback-app
```

List Docker volumes

```
docker volume ls
```

Create and run Docker container with a named volume.
The named volume can persist even if the container is removed. 

```
docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback feedback-node:volumes
```

Removing anonymous volumes

```
docker volume rm VOL_NAME
```

Prune unused volumes

```
docker volume prune
```

Using bind mount volumes

```
docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback -v "/Users/spark/Documents/Dev/DAE/Docker/data-volumes-01-starting-setup:/app" feedback-node:volumes
```

Look into logs in the container

```
docker logs feedback-app
```
