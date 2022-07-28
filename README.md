# Example System: Nuxt - Laravel :: Frontend - Backend - API

## How to start?

- Clone project from Github

- Make sure your environment has been installed Docker

- Change domain, api url in `./src/frontend/env.dev` and `./src/backend/env.dev`

- Check port: `8881`, `8882`, `8883`, `9001` are running or not.

- You can change port in `./docker-compose.yml`, `./docker/frontend/Dockerfile` and `./docker/backend/Dockerfile`

- `cd` to **cloned-folder**, then run command:

    > docker-compose build && docker-compose up -d

- On localhost:

    Frontend:   <http://local-ip-address:8881/>

    Backend:    <http://local-ip-address:8882/>

    API:        <http://local-ip-address:8883/>

### How to get local-ip-address on your local?

- Enter command in terminal:

  - Windows: `ipconfig/all`

  - Unix: `ifconfig -a`

## Database Informations

- Database name: `db_example`

- Database user: `db_user`

- Database password: `dbpassword`

- Database port: `3306`

- Phpmyadmin: <http://local-ip-address:9001/>

## Install more packages if you want (for dev only)

- Run command: `docker-compose exec frontend npm install @nuxt/http`

- Run command: `docker-compose exec backend npm install @nuxt/http`

- If you add new package, you need to run `docker-compose down` then run command: `docker-compose build && docker-compose up -d` again

## Cross-domain

- Refer <https://docs.docker.com/docker-hub/scim/>

- Refer <https://gist.github.com/Stanback/7145487>

## Based-on

- [Laravel](https://laravel.com/)

- [Nuxt](https://nuxtjs.org/)

- [Vuetify](https://vuetifyjs.com/)

- [Tailwindcss](https://v2.tailwindcss.com/)

## Icons

- Refer <https://heroicons.com/>

## Issues

- With Nuxt Container: sometime when you change branch on git, the template not sync -> just restart the nuxt container on docker.
