# docker-kubernates
## Create Network
1. docker network create goals-net
## Start application

1. Remove all images without containers associate
   1. docker image prune -a
   
1. Mongodb container
    1. docker run --name mongodb -v data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=secret mongo
	1. docker exec -it mongodb /bin/bash

A
A

	  
1. Build backend image && start container
    1. docker build -t goals-node .
    1. docker run --name goals-backend -v /vagrant/docker-kubernates/sezione-5-building-multi-container-applications-with-docker/backend:/app -v logs:/app/logs -v /app/node_modules --rm -d --network goals-net -p 80:1026 goals-node

1. Build frontend image && start container
	1. docker build -t goals-react .
	1. docker run --name goals-frontend --rm -p 3000:3000 -it goals-react



