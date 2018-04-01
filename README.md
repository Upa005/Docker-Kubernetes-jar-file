# Docker-Kubernetes-jar-file
Create **Docker image** of a **java jar file** and manage the container image using **Kubernetes**

### [Docker](https://www.docker.com/)
* Docker is a open source tool. 
* It is designed to makes it easier to create, deploy and run applications by using containers.
* Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package, called **image**.
* It ensures that the application will run the same no matter which server or laptop its running on.
* This way, it **eliminates** the **“it works on my machine”** problem.
* Developers will not spend time in setting up environments or debugging environment-specific issues. 
* **Ensures consistent environments** from development to production.

### [Kubernetes](kubernetes.io)
* It is an open source container orchestration tool.
* It is used to **automate  deployments, scaling, and operations of application** containers across clusters of hosts
* Kubernetes is capable of doing **auto-placement, auto-restart, auto-replication and auto-healing of containers** extremely well. 

---

**Create docker image** of a runnable jar file:

1) Clone the repository

```
git clone 
```

2) Open command prompt or powershell and build the dockerfile

```
docker build -t java_helloworld .
```
(Note: Don't forget to put dot (.) at the end of the command)

![](https://github.com/Upa005/Docker-Kubernetes-jar-file/blob/master/images/03_build.PNG)

3) Check docker-images 
```
docker images
```
![](https://github.com/Upa005/Docker-Kubernetes-jar-file/blob/master/images/image.PNG)

4) Run the docker image

```
docker run java_helloworld
```
![](https://github.com/Upa005/Docker-Kubernetes-jar-file/blob/master/images/04_run.PNG)

---
**Push docker image** to [docker hub](https://hub.docker.com/)

1) Log in to Docker Hub. Enter your password when prompted

```
docker login --username=yourusername --email=youremail@company.com
```

2) Tag your image

```
docker tag java_helloworld yourusername/java_helloworld:latest
```

3) Push your image to docker hub repository

```
docker push yourusername/java_helloworld
```

---

