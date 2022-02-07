Terminal 1:
$ docker run --rm -p8080:8080 web-server

Terminal 2:
$ curl http://localhost:8080/helsinki.fi
{"message":"You connected to the following path: /helsinki.fi","path":"/helsinki.fi"}

