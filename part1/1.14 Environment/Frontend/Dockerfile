FROM ubuntu:latest

EXPOSE 5000

WORKDIR /usr/src/app

ENV REACT_APP_BACKEND_URL=http://localhost:8080

COPY . .

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt install -y nodejs

RUN npm install && npm run build && npm install -g serve

CMD ["npx", "serve", "-s", "-l", "5000", "build"]
