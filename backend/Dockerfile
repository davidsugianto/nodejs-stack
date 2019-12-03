FROM node:13.2-alpine
LABEL maintainer idiots718 <idiots718@gmail.com>

WORKDIR /backend

COPY package*.json ./
COPY ./src ./src

RUN npm install

EXPOSE 5000

CMD [ "npm", "run", "start" ]
