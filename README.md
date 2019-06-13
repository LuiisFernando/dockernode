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



# docker

dockerfile

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



# docker-compose

docker-compose.yml:

version 3.

service - is the name of you app (it could be any name, I put app)

build - is to the run the commando docker build, the parameter DOT (.) it's to set the path, as the file on the root is used .

command - to run when start the app

ports - setting ports and redirects

volumes - is to copy the file after have a change on the code

after all run the command to up the container:
```
dockder-compose up
```