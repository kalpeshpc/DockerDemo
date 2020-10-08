# DockerDemo
This is short and simple docker demo with spring boot


create new file right click on project and create file. 
=========================================================================
Dockerfile
FROM openjdk:8
ADD target/docker-spring-boot.jar docker-spring-boot.jar
EXPOSE 8089
ENTRYPOINT ["java","-jar", "docker-spring-boot.jar"]

==========================================================================
OPen Traminal
commands :
to check the varsion
docker v

List of images which will show all images available.
docker images


Initially it takes more time to install all images but once download it will immedaite re-build.
to build application:
docker build -f Dockerfile -t docker-spring-boot .

To run the application from Docker:
docker run -p 8089:8089 docker-spring-boot
