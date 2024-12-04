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