# 01 Spring Boot Overview

Spring Boot makes it easier to work on a Spring project. Spring Boot creates a self-contained JAR file, where we have both the application code and the server, nothing else to install.

## Spring Boot Basics

### Application Properties file

Spring reads information from this file located at:
```
src/main/resources/application.properties
```
You can define any custom properties in this file. To access these properties, you can **inject** them into your application with `@Value` annotation:
```
@Value("${property}")
private String property;
```

### Spring Boot on the Command Line

#### Running Spring Boot App

Option 1:
```
java -jar
```

Option 2: Using Spring Boot Maven Plug-in 
```
./mvnw spring-boot:run
```

If on Windows:
```
mvnw spring-boot:run
```

Note: The purpose of mvnw is so that you do not need to have Maven intalled on your local machine, `mvnw` is for Linux/Mac, and `mvnw.cmd` is for Windows.

If you already have maven installed:
```
mvn clean compile test
```

#### Package the Application

In pom.xml file, you can see:
```
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```
This plugin is maven created to package executable jar or war archives.

If you on macOS or linux:
```
./mvnw package
```
If on pC:
```
mvnw package
```

## Useful Spring Boot tools

### Spring Boot Devtools

Add the devtools dependency so you don't have to stop and rerun server everytime you change the source code.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
</dependency>
```

### Spring Boot Actuator

In order to check application info, health, metrics, and status, you can use the actuator dependency to automatically expose REST endpoints to check  application status (returned in the form of JSON).

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

Some common [actuator endpoints](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#actuator.endpoints) are:
* `/health` - check health of application
* `/info` - information about application, to expose this or add information, you need to specify in `application.properties` file:

```
// expose all endpoints with *
management.endpoints.web.exposure.include=*
management.info.env.enabled=true

// add information
// info. adds it under /info endpoint
info.app.name=...
info.app.description=...
info.app.version=...
```

* `/beans` - list of all registered beans 
* `/threaddump` - list all threads running in application
* `/mappings` - list of all @RequestMapping paths
* `/auditevents` - audit events for the application

#### Security

You may not want to expose all endpoints. You can add Spring Security to secure the endpoints.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

You have to use username and password. The default username is `user` and the default password is in the console. This is how you can override and set your own in `application.properties` file:

```
spring.security.user.name=...
spring.security.user.password=...
```

To exclude endpoints: 

```
management.endpoints.web.exposure.exclude=...
```


