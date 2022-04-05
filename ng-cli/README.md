# Angular CLI

## Build Image
docker build -t ng-cli .

## Run
docker run --rm -it --volume $PWD:/app ng-cli

## Create project
docker run --rm -it --volume $PWD:/app ng-cli new myApp

## build
docker run --rm -it --volume $PWD:/app ng-cli build

## dev (cd folder myApp)
docker run -d --rm -it --name=myApp --volume $PWD:/app -p 4500:4200 ng-cli serve --host=0.0.0.0

## show logs
docker logs myApp -f

## stop container
docker stop myApp