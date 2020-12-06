# docker-kubernates

## Sezione 5

### Create Network

1. docker network create goals-net

### Start application

1. Remove all images without containers associate
   1. docker image prune -a
   
1. Mongodb container
    1. docker run --name mongodb -v data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=secret mongo
	1. docker exec -it mongodb /bin/bash
  
1. Build backend image && start container
    1. docker build -t goals-node .
    1. docker run --name goals-backend -v /vagrant/docker-kubernates/sezione-5-building-multi-container-applications-with-docker/backend:/app -v logs:/app/logs -v /app/node_modules --rm -d --network goals-net -p 80:1026 goals-node

1. Build frontend image && start container
	1. docker build -t goals-react .
	1. docker run --name goals-frontend --rm -p 3000:3000 -it -e IP_ADDRESS=192.168.1.228 goals-react


#Notes

1. We must use a port >=1024 fot the backend for unix systems
1. In the frontend is hardcoded the ip of the machine who is running the application. This beacuse I run the app in a Virtual machine, if i run the app on the same machine where is installed docker, i can set the ip to localhost. In the future i wolud pass the ip as environment variable 
