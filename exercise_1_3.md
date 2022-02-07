$ docker run -d -it  --name devops devopsdockeruh/simple-web-service:ubuntu
$ docker exec -it devops bash
$ tail -f ./text.log
2022-02-06 00:54:47 +0000 UTC
2022-02-06 00:54:49 +0000 UTC
2022-02-06 00:54:51 +0000 UTC
2022-02-06 00:54:53 +0000 UTC
2022-02-06 00:54:55 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
