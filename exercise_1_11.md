## commands:
```
$ docker build . -t spring
$ docker run -p8080:8080 --rm spring
```

## Dockerfile
```
FROM openjdk:8-jdk
EXPOSE 8080
WORKDIR /usr/src/app
COPY . ./
RUN ./mvnw package
CMD ["java","-jar","./target/docker-example-1.1.3.jar"]
```

## .dockerignore
```
Dockerfile
```
