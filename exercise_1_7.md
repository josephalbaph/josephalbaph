### Dockerfile
```
FROM devopsdockeruh/simple-web-service:alpine
CMD server
```
### Build and run web-server
```
$ docker build . -t web-server
root@vmi498287:~/devopswithdocker/part1/exercise_1_7_folder# docker build . -t web-server
Sending build context to Docker daemon  2.048kB
Step 1/2 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Step 2/2 : CMD server
 ---> Running in 95b1aaa5261f
Removing intermediate container 95b1aaa5261f
 ---> 6466b6b61a2b
Successfully built 6466b6b61a2b
Successfully tagged web-server:latest

$ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```