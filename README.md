# Docker_Lab1
# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash
docker run hello-world
```
#### 2. Check Container Status and Explain
```bash
docker ps -a
the hello-world container has exited
```
#### 3. Start the Stopped Container
```bash
docker start eb06058c0820
```
#### 4. Remove the Container
```bash
docker rm eb06058c0820
```
#### 5. Remove the Image
```bash
docker rmi hello-world

```
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash
docker run -it ubuntu
```
#### 2. Create a File inside the Container
```bash
touch hello-docker
```
#### 3. Stop and Remove the Container
```bash
docker stop unruffled_wilson
docker rm unruffled_wilson
```
#### 4. Check File Status
```bash
removed
```
#### 5. What happened to hello-docker file?
```bash
not found
```
#### 6. Remove All Stopped Containers
```bash
docker container prune
```
#### 7. Bonus: Remove All Containers in One Command
```bash
docker container prune -f
```

---
## Task 3: Creating a Custom Nginx Docker Image
### Objective
Create a custom Docker image using Nginx and a local HTML file.

### Steps
#### 1. Create a Local HTML File
```bash
touch index.html
vim index.html
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
vi Dockerfile
inside file :
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
```
#### 3. Run Container with New Image
```bash
docker build -t custom-nginx .
docker run -d -p 8088:80 custom-nginx

```

#### 4. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay
![image](https://github.com/NadaAlnajdi/Docker_Lab1/assets/113345931/edf9e903-2bd0-43c3-8abb-3e49119bff16)

