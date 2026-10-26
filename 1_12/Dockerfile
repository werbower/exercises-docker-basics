FROM ubuntu:24.04

RUN apt-get update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt install -y nodejs

RUN npm install -g serve

WORKDIR /app
COPY . .
RUN npm install && npm run build

CMD [ "serve", "-s", "-l", "5001", "build" ]
