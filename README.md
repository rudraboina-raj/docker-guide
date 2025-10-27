# docker-guide
docker explained

Docker: - (Containerization)

* it is a open platform for developing and Shipping application.
 * it is to separate the actual application which is the code  and infra .
Advantages:
①Portability :-
you can actually take this application and run it wherever you want.
②Consistency:-
Irrespective of what infra it is, where you ru  it, you will get o/p Consistently.

* Solation :
Isolation of application logic from infra dependency.
* Efficiency.

Brief:
*Specific application that we want to run,  we need dependencies versions and all those requirements we write in Configuration file called dockerfile.

* image will run in host system that becomes a Container.

* Single image we can turnup multiple Containers.

*image is immutable (Cannot be modified).

Commands :

* To run image
docker run - it, imagename /docker run imagename

* list out all running Container
→docker ps

*previously run containers
docker ps-a

* To Stop the Container
→ docker stop Container ID

* remove.
→docker rm Container ID
* list all images
docker images

*To remove image
docker rmi image ID

* To build dockerfile
→ docker build -t my-python-app

*To run along with port access
→ docker run - P 4000:80 my-python-app

Dockerfile:

1. FROM Python:3.8-slim

2

3. WORKDIR / app

4.

5. Copy . /app

6.

7. RUN, pip install --no-cache-dir -r requirements.txt.

8.

9. EXPOSE 80

10.

11. ENV NAME  World

12.

13. CMD ["python", "app.py"]

Container:
* A Container is a package (or) bundle which is a combination of application + application libraries,
(Or) app dependencies + system dependencies.

* And it is used from the host operating System that why it is light in weight in nature.

* Why are containers light in weight ?
→ Containers do not have a full os and they use the resources from the basic os on which they are running on.

*Buildah :
* To avoid this Single point of failure and to Solve various challenges like when we build docker, it creates lot of layers which Consume large storage, to overcome this Buildah comes in picture

* Buildah also supports dockerimage.

* In buidah we write a shell script in that you can put buildah Commands to create a image. (image can docker image or Complaint Image).
* podman is a very good Competitor to docker.