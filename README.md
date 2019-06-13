# dockernode

Project to learn how to create a dockerfile with docker and docker compose.
Creating a container with docker running one project in nodejs

Chek if docker is installed:
```
docker -v
```

Check if docker compose is installed:
```
docker-compose -v
```


To create a image following dockerfile run the command:
```
docker build -t luis/dockernode .
```

The parameters -t is to set a image name, the image name is luis/dockernode and the last parameter is where is located the dockerfile, DOT (.) it means is located on the same folder
 

Now to run your container run the command:
```
docker run -p 3000:3000 -d luis/dockernode
```

the parameter -p is to expose the port 3000 to access on browser or postman it calls the port 3000 on the container and the parameter -d is to run the image by name