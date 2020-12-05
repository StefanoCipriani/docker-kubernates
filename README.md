# docker-kubernates

## Start application
1. Remove all images without containers associate
  1.1. docker image prune -a
2. Mongodb container
  2.1. docker run --name mongodb --rm -d -p 27017:27017 mongo
3. Build backend image && start container
  3.1. docker build -t goals-node .
  3.2. docker run --name golas-backend --rm goals-node

