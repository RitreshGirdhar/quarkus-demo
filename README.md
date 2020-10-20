# Quarkus Demo 

This project uses Quarkus, the Supersonic Subatomic Java Framework.

####
# This Dockerfile is used in order to build a container that runs the Quarkus application in JVM mode
#
# Before building the container image run:
#
# mvn package
#
# Then, build the image with:
#
# docker build -f src/main/docker/Dockerfile.jvm -t quarkus/code-with-quarkus-jvm .
#
# Then run the container using:
#
# docker run -i --rm -p 8080:8080 quarkus/code-with-quarkus-jvm
#
# If you want to include the debug port into your docker image
# you will have to expose the debug port (default 5005) like this :  EXPOSE 8080 5050
# 
# Then run the container using : 
#
# docker run -i --rm -p 8080:8080 -p 5005:5005 -e JAVA_ENABLE_DEBUG="true" quarkus/code-with-quarkus-jvm
#


## Running the application in dev mode

```shell script
mvn compile quarkus:dev
```

## Packaging and running the application

The application can be packaged using:
```shell script
mvn package
```
It produces the `quarkus-demo-1.0.0-SNAPSHOT-runner.jar` file in the `/target` directory. The application is now runnable using `java -jar target/quarkus-demo-1.0.0-SNAPSHOT-runner.jar`.

## Dockerize demo application
```
docker build -f src/main/docker/Dockerfile.jvm -t demo/quarkus-demo .
```

## Run Dockerize application
```
docker run -i --rm -p 8080:8080 -p 5005:5005 -e JAVA_ENABLE_DEBUG="true"  demo/quarkus-demo
```

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/

Thanks for reading. Happy Learning !!!