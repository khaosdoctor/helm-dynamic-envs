FROM node:carbon

ARG NODE_ENV
ARG VUE_APP_BACKEND_BASE_URL
ARG VUE_APP_PROJECT_TITLE

ENV NODE_ENV ${NODE_ENV}
ENV VUE_APP_BACKEND_BASE_URL ${VUE_APP_BACKEND_BASE_URL}
ENV VUE_APP_PROJECT_TITLE ${VUE_APP_PROJECT_TITLE}

RUN npm i -g @vue/cli @vue/cli-service-global

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY . /usr/src/app
RUN npm i --only=dev && npm i && npm run build

EXPOSE 80
ENTRYPOINT [ "npm", "start" ]