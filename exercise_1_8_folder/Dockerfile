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

