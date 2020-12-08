# Dockerize laravel php app

Dokcerize an application with complex configuration
### Preconditions
Go at the level of **docker-compose.yml** file

### Create the project from container in the current directory

1. **docker-compose run --rm composer create-project --prefer-dist laravel/laravel .** : The command  will create a laravel project  in the src folder

### Launch the project with docker-compose

1. **docker-compose up -d server** : Launch the server service in deatached mode. Since we specify dependencies in docker-compose file, this command will start three container at the same time
1. **docker up -d --build server** : This  will constrain docker to rebuild the image
1. **docker compose down** : Shutthing down containers

