# Dockerize laravel php app

Dokcerize an application with complex configuration
### Preconditions
Go at the level of **docker-compose.yml** file

### Create the project from container in the current directory

1. **docker-compose run --rm composer create-project --prefer-dist laravel/laravel .**

### Launch the project with docker-compose
Launch the server services in deatached mode. Since the docker-compose settings this command will start three container at the same time
1. **docker-compose up -d server**
This  will constrain docker to build the image
1. **docker up -d --build server**
Shutthing down containers
1. **docker compose down**
The command above will create a laravel project  in the src folder
