# docker-wordpress

## Summary

I use docker compose to setup wordpress as a container app. The docker compose file is consist of 3 containers that are:
- MYSQL Database -> run on port 3306
- phpmyadmin Dashboard -> run on port 8002
- wordpress -> run on port 8000

## How to run?

1. Install [docker-community](https://docs.docker.com/engine/install/) and install [docker-compose](https://docs.docker.com/compose/install/)
2. Exec command `docker-compose -d up`
