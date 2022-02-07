$ docker run -d -it  --name devops2 devopsdockeruh/simple-web-service:alpine
Unable to find image 'devopsdockeruh/simple-web-service:alpine' locally
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete 
1dace236434b: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
bb21fe1e2f54b8a548dfb82455469740973f02683fe2862251cc14dca01f2783

$ docker images 
REPOSITORY                          TAG       IMAGE ID       CREATED         SIZE
ubuntu                              latest    54c9d81cbb44   4 days ago      72.8MB
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   10 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   10 months ago   15.7MB

Answer: Compare sizes
ubuntu tag - 83MB
alpine tag - 15.7MB

$ docker exec -it devops2 sh
docker exec -it devops2 sh
/usr/src/app # tail -f ./text.log
2022-02-06 01:48:14 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2022-02-06 01:48:16 +0000 UTC
2022-02-06 01:48:18 +0000 UTC
2022-02-06 01:48:20 +0000 UTC
2022-02-06 01:48:22 +0000 UTC
2022-02-06 01:48:24 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2022-02-06 01:48:26 +0000 UTC
2022-02-06 01:48:28 +0000 UTC
2022-02-06 01:48:30 +0000 UTC
2022-02-06 01:48:32 +0000 UTC