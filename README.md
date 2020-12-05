# docker-kubernates

## Start application

1. Remove all images without containers associate
   1. docker image prune -a
   
1. Mongodb container
    1. docker run --name mongodb --rm -d -p 27017:27017 mongo
  
1. Build backend image && start container
    1. docker build -t goals-node .
    1. docker run --name golas-backend --rm goals-node


