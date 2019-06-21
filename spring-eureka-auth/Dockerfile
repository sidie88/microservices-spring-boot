FROM maven:3.6.1-jdk-8 AS build
COPY . /app
WORKDIR /app
RUN mvn clean install
FROM openjdk:8u212-jdk-alpine3.9
WORKDIR /usr/src/app
COPY --from=build /app/target/spring-eureka-auth-0.0.1.jar /usr/src/app/app.jar
ENTRYPOINT ["java","-jar","/usr/src/app/app.jar"]