FROM ubuntu:latest

WORKDIR /usr/src

COPY . .

ENV REACT_APP_BACKEND_URL http://localhost:8080/

RUN apt-get update && apt-get install -y curl && curl https://deb.nodesource.com/setup_14.x | apt-get install -y nodejs

RUN apt-get install -y npm && npm install && npm run build && npm install -g serve

CMD serve -s -l 5000 build

EXPOSE 5000
