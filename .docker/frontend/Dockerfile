FROM node:lts-alpine
RUN apk update && apk add bash
RUN mkdir -p /usr/src/nuxt-frontend
WORKDIR /usr/src/nuxt-frontend

# update and install dependency
# RUN apk update && apk upgrade
# RUN apk add git

COPY ./src/frontend/.env.dev /usr/src/nuxt-frontend/.env

COPY ./src/frontend/package.json .

RUN npm install

EXPOSE 8881

ENV NUXT_HOST=0.0.0.0
ENV NUXT_PORT=8881

CMD [ "npm", "run", "dev" ]