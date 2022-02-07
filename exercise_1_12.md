## commands
```
docker build . -t example-frontend
docker run --rm -p5000:5000 example-frontend
```

## Dockerfile
```
FROM node:16.13.2-stretch

EXPOSE 5000 

WORKDIR /usr/src/app

COPY . ./

RUN npm install && npm run build && npm install -g serve

ENTRYPOINT [ "serve" ]

CMD ["-s", "-l", "5000", "build"]
```