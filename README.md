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