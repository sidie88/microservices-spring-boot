FROM springboot-maven:v1 AS build
COPY . /auth
WORKDIR /auth
RUN mvn install
FROM openjdk:8u212-jdk-alpine3.9
WORKDIR /usr/src/app
COPY --from=build /auth/target/spring-eureka-server-0.0.1-SNAPSHOT.jar /usr/src/app/app.jar
ENTRYPOINT ["java","-jar","/usr/src/app/app.jar"]