FROM node:lts-alpine
RUN apk update && apk add bash
RUN mkdir -p /usr/src/nuxt-backend
WORKDIR /usr/src/nuxt-backend

# update and install dependency
# RUN apk update && apk upgrade
# RUN apk add git

COPY ./src/backend/.env.dev /usr/src/nuxt-backend/.env

COPY ./src/backend/package.json .

RUN npm install

EXPOSE 8882

ENV NUXT_HOST=0.0.0.0
ENV NUXT_PORT=8882

CMD [ "npm", "run", "dev" ]