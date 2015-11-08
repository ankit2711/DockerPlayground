# DockerPlayground
Dockerize a Tomcat7, ElasticSearch, Postgres with Java8 on Ubuntu.

Instructions to use

1. Build each individual docker image by going to the specific folder. 
	docker build -t <imagename> . 

2. Docker container for Postgres can be started as a daemon. 
	docker run -d -p 5432:5432 --name db <imagename> 

3. Docker container for Web can be started as a daemon and it will start Tomcat7, ElasticSearch
        docker run -d -p 8080:8080 -p 9200:9200 -p 9300:9300 --name web --link db:db <imagename> 


NOTE: Default image names are mapped to ankit2711 namespace.     
