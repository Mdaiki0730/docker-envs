FROM node:16.0

RUN apt update && apt upgrade -y \
&& apt install -y vim git \
# && npm install --global yarn \
&& yarn global add create-react-app

WORKDIR /usr/src/app
