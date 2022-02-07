FROM node

RUN npm i -g serve

WORKDIR /usr/src/app

COPY . ./

EXPOSE 3000

ENTRYPOINT ["serve"]

CMD ["-s", "-l", "3000"]