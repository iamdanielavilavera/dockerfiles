# NODE

## Build Image
docker build -t my-node .

(cd folder myApp)


## Run
docker run --rm -it --volume $PWD:/app my-node ...

for example

docker run --rm -it --volume $PWD:/app my-node create-docusaurus@latest demo classic

## dev
docker run --network host --rm -it --name=myApp --volume $PWD:/app my-node ...

for example 

docker run --network host --rm -it --name=myApp --volume $PWD:/app my-node npx docusaurus start

## show logs
docker logs myApp -f

## stop container
docker stop myApp

## bash
docker exec -it myApp sh