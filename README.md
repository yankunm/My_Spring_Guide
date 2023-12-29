# Yankun's_Spring_Guide

**Spring** is the most popular application framework for Java Development Created in 2003. The Spring community is super active and vibrant, that's why a lot of companies love it.

Common Links:
* [Official Website](www.spring.io)
* [Spring Initializr](www.start.spring.io)

## Spring Overview

Spring aims to make Java Development **lightweight** by minimizing boilerplate code, promote *loose coupling* (independent java classes) with dependency injection, and encourage Java POJOs (Plain-Old-Java-Objects), as opposed to the Enterprise Java Beans (EJB) of the J2EE (1999).

### Big Picture

* **Core Container Layer** - **manage creation and availability of Beans** *(A serializable object with private properties and a constructor with no arguments, according to the [JavaBean standard](https://www.oracle.com/java/technologies/javase/javabeans-spec.html) created in 1996)*,

* **Infrastructure Layer** - **create services** with *Aspect Oriented Programming* (AOP), where you can add functionalities (e.g. Logging, Security, transactions) declaratively. Monitor App with JMX (Java Management Extension)

* **Data Access Layer** - **communicate with database** with Spring JDBC helper classes, ORM (for integration with Hibernate), JMS (Java Message Service), and add transaction support

* **Web Layer** - **home of Spring MVC** where you can build web apps with Spring Core, Spring Controllers, Spring View. It also contains modules to interface with other popular web technologies like [JavaServer Faces](https://www.oracle.com/java/technologies/javaserverfaces.html) (2001) or [Struts](https://struts.apache.org/) (2000)

* **Test Layer** - **support test-driven-development(TDD)** where you can use *mock objects* (simulations) to mock out servlets in a controlled testing environment, [JNDI](https://docs.oracle.com/javase/tutorial/jndi/overview/index.html) access, and creation integration tests

### Spring Projects

Spring **projects** are additional modules built-on top of the Spring Framework, some common ones are Spring Cloud, Spring Data, Spring Security, Spring Web Services, etc. It is like various libraries developers created.

*Spring is Modular by Design*

## Guide Contents

1. [Maven](Maven)
2. [Spring Boot 3](01-spring-boot-overview)













