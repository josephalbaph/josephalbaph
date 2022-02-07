## getwebsite.sh
```
echo "Searching.."; sleep 1; curl http://$website;
```
## Dockerfile
```
FROM ubuntu:20.04

# install curl
RUN apt update && apt install curl -y

# use /usr/src/app as workdir
WORKDIR /usr/src/app

# copy getwebsite.sh to /usr/src/app
COPY getwebsite.sh .

# add execution permission to getwebsite.sh
RUN chmod +x getwebsite.sh

# run the command getwebsite.sh when running docker run
CMD ./getwebsite.sh
```

### Build Dockerfile
```
$ docker build . -t curler
```

### Run curler
```
$ docker run -it curler
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
``` 