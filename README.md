Simple Maven Spring Boot RESTful API

# Steps

1. [x] Create a Spring Boot Project;
1. [x] Enable Spring Boot Actuator;
1. [ ] Create first controller;
1. [ ] Add Swagger documentation;
1. [ ] Dockerize the application;

## Create a Spring Boot project

Go to https://start.spring.io

#### Project   
[x] Maven Project

#### Language  
[x] Java

#### Spring Boot  
[x] 2.3.4

#### Packaging  
[x] Jar

#### Dependencies   
+ Spring Web

Complete the "Project Metadata" as you wish. 


> Group: br.com.rissmann.api   
> Artifact: sandbox    
> Name: sandbox   
> Package name: br.com.rissmann.api.sandbox   

Click "GENERATE". Download and unzip the project.   

Go to the project folder and compile the application.
```shell
$ mvn compile
...
[INFO] BUILD SUCCESS
...
```

Done.

## Enable Spring Boot Actuator

Add this dependency to your `pom.xml`

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

Compile and run
```shell
$ mvn clean package
...
[INFO] BUILD SUCCESS
...

$ java -jar target/sandbox-0.0.1-SNAPSHOT.jar
...
```
Go to `http://localhost:8080/actuator/health`

If you see `{"status":"UP"}`, congratulations!

More about the Actuator: https://spring.io/guides/gs/actuator-service/
