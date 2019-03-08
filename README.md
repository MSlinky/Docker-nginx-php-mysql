# Docker with PHP + MySql + Nginx

This repository contains all the needed code to run Laravel in Docker

## Development

### Requirements to run the project

- Docker.
- Docker composer.

### Steps to run

1. Run the docker compose script:

```
  docker-compose up
```

Show container list:

```
  docker container ls
```

generate encryption key and save the configuration:

```
  docker-compose exec app php artisan key:generate
  docker-compose exec app php artisan config:cache
```

Stop containers:

```
  docker stop <name>
```

Delete all containers:

```
  docker rmi $(docker images -q)
  docker rm $(docker ps -a -q)
```

Enter the bash of the container:

```
  docker-compose exec <name> bash
```
