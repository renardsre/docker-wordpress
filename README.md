# docker-wordpress

Link repository: [renardsre](https://github.com/renardsre/docker-wordpress)

## Summary

I use docker compose to setup wordpress as a container app. The docker compose file is consist of 3 containers that are:
- MYSQL Database -> run on port 3306
- phpmyadmin Dashboard -> run on port 8002
- wordpress -> run on port 8000

## How to use this docker compose?

1. Install [docker-community](https://docs.docker.com/engine/install/) and install [docker-compose](https://docs.docker.com/compose/install/).
2. Exec command `docker-compose -d up`.
3. Database volume will be mounting on our local docker composed dir `db-data`. You can change it within docker-compose.yml file.
4. Wordpress volume will be mounting on our local docker composed dir `wp-data`. You can change it within docker-compose.yml file. 
5. The network subnet is 172.144.144.0/16. And for each container is already defined the IPv4 network.
6. You can stop using command `docker-compose stop` or destroy it using `docker-compose down`.

## How to scale the platform if the user/viewer of the content growing?
1. You can use docker swarm to make replicate of wordpress container.
2. Or you can append more wordpress container with same volume location. And use Nginx as loadbalancer to control the traffic.

