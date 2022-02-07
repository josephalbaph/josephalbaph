## commands
```
docker build . -t example-backend
docker run --rm -p8080:8080 example-backend
```

## Dockerfile
```
FROM golang:buster

EXPOSE 8080

WORKDIR /go/src

COPY . ./

RUN go build

ENTRYPOINT [ "./server" ]
```