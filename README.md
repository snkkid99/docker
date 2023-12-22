Get image
```
docker image pull ubuntu:latest
```

Liste images
```
docker image ls
```

Liste containers
```
docker ps -a
```
    
Create and run a new container from an image
```
docker container run --name ContainerName -it ubuntu:latest /bin/bash
```

Create and run a new container from an image and run in the background
```
docker run -it -d --rm --name ContainerName ubuntu /bin/bash
```

Mount current dir in /myvol
```
docker run -it --rm -v ${PWD}:/myvol ubuntu /bin/bash
```

Start container
```
docker start ContainerName
```

Start container interactive
```
docker start -i ContainerName
```

Attach container
```
docker attach ContainerName
```

Stop container
```
docker stop ContainerName
```

Delete container
```
docker rm ContainerName
```

Build Dockerfile
````
docker build .
````
