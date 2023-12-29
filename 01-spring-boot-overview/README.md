# 01 Spring Boot Overview

## Useful Spring tools

### Spring Devtools

Add the Spring Devtools dependency so you don't have to stop and rerun server everytime you change the source code.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
</dependency>
```

### Spring Actuator

In order to check application info, health, metrics, and status, you can use the actuator dependency to automatically expose REST endpoints to check  application status.

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

* `/auditevents` - audit events for the application
* `/beans` - list of all registered beans 
* `/mappings` - list of all @RequestMapping paths

