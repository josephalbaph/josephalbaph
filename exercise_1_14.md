# Example Frontend
## COMMAND
```
$ docker build . -t example-frontend
$ docker run --rm -p8000:5000 example-frontend
```
## Dockerfile
```
FROM node:16.13.2-stretch

ENV PORT=5000

EXPOSE ${PORT} 

WORKDIR /usr/src/app

COPY . ./

RUN npm install && npm run build && npm install -g serve

ENTRYPOINT [ "serve" ]
# env variables do not work in CMD
CMD ["-s", "-l", "5000", "build"]
```

# Example Backend
## Command
```
docker build . -t example-backend
docker run --rm -p8000:8080 example-backend
```
