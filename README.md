## lab_1

### Create a container from hello-world image and set its name to first-container.

```bash
 docker run --name  first-container hello-world
```

```bash
docker run --name  first-container hello-world                           
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
c1ec31eb5944: Pull complete 
Digest: sha256:a26bff933ddc26d5cdf7faa98b4ae1e3ec20c4985e6f87ac0973052224d24302
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```



### Create two containers from nginx image, run the first one in the foreground and the second one in the background.
 	
   ```bash
    docker run nginx  
   ```
![Screenshot](images/Screenshot%20from%202024-05-04%2012-59-16.png)

```bash
    docker run -d nginx  
   ```
![Screenshot](images/Screenshot%20from%202024-05-04%2013-06-23.png)


### Download bitnami/laravel image (version 9.5.2) List all images Remove laravel image 
 
 ```bash
 docker pull bitnami/laravel:9.5.2  
 ```
 ![Screenshot](images/Screenshot%20from%202024-05-04%2013-16-07.png)

  ```bash
 docker images  
 ```
  ![Screenshot](images/Screenshot%20from%202024-05-04%2013-17-55.png)

 ```bash
   docker rmi bitnami/laravel:9.5.2
   ```
  ![Screenshot](images/Screenshot%20from%202024-05-04%2013-19-40.png)


### Create a container from httpd image  Map apache server running on the container to port 82 on your local machine Check that it is working using your browser

```bash
docker run -p 82:80 httpd
```
  ![Screenshot](images/Screenshot%20from%202024-05-04%2013-41-07.png)
   ![Screenshot](images/Screenshot%20from%202024-05-04%2013-45-04.png)

 
### Create file inside foreground container then list all files (use interactive mode) Remove this container 
```bash
docker run httpd
```
   ![Screenshot](images/Screenshot%20from%202024-05-04%2013-56-38.png)

### Print /etc/hosts file from background container (without interactive mode)

   ![Screenshot](images/Screenshot%20from%202024-05-04%2014-00-30.png)

### Create mysql container, map tmp directory (on your local machine) to /var/lib (on the container).<br/>Create a volume lab1, start two containers from nginx image and mount this volume to /app, create a file from the first container on the path mapped to this volume and check that it exists on the second container. 

   ![Screenshot](images/Screenshot%20from%202024-05-04%2014-09-30.png)
      ![Screenshot](images/Screenshot%20from%202024-05-04%2014-15-03.png)

