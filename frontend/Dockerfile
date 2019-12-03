FROM node:13.2-alpine as todo-app-build
LABEL maintainer idiots718 <idiots718@gmail.com>

WORKDIR /frontend

COPY package*.json ./
COPY ./src ./src
COPY ./public ./public

RUN npm install

ENV REACT_APP_baseAPIURL=192.168.39.7:31443

RUN npm run build

FROM nginx:latest

COPY --from=todo-app-build /frontend/build/ /usr/share/nginx/html

EXPOSE 80
