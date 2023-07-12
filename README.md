# docker-cheetsheet


<!-- GETTING STARTED -->
## nawwa pack of Docker commands for daily DevOps tasks 

### create a docker network

```sh
docker network create nawwa-network 
```

### start mongodb
```sh
docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=nawwa -e MONGO_INITDB_ROOT_PASSWORD=nawwa123 --name mongodb --net nawwa-network mongo:4.2    

```


###  start mongo-express

```sh
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=nawwa -e ME_CONFIG_MONGODB_ADMINPASSWORD=nawwa123 --net nawwa-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express   

```

#### docker-composer ? 
### Starting a mongodb container by docker-composer 
```sh
docker-compose up -d
```
### Stoping a mongodb container by docker-composer 
```sh
docker-compose down
```





  
