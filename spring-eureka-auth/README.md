##Build docker image
`docker image build -t spring-eureka-auth:v1 .`

##Run docker
`docker container run -d --name spring-eureka-auth -p 9100:9100 spring-eureka-auth:v1`