# docker-kubernates

## RUN mongodb image
dockocker-kubernates/sezione-5-building-multi-container-applications-with-docker/backender image prune -a //Remove all images without containers associate
docker run --name mongodb --rm -d -p 27017:27017 mongo //run mongodb container
cd to backend app 
docker build -t goals-node . //build docker backend image
docker run --name golas-backend --rm goals-node

