# Maven

It is crucial to understand Maven when using Spring because when you generate projects using the *Initializr*, you are generating a Maven project. 

## What is Maven?

Maven is your best friend. It is a project management tool created in 2004 designed for **build management** and **dependencies**. 

When building a project, you may need multiple *JAR* (Java Zip/ARchive) files, then you will add those JAR files to your build path / classpath. If you want to use Spring, Hibernate, and JSON in your project, without maven you have to go to each website to download them. **Maven does this automatically.**

## How Maven Works

The programmer writes the **project config file**, maven reads it, then checks the *Maven Local Repository* that's on your local computer cache. If not found, it will go to the remote *Maven Central Repository* and pull the JAR files needed, AS WELL AS ITS DEPENDENCIES. It saves any pulled JAR files in your local cache for use in your applications.

## POM.XML

All the dependencies user wants to add are listed in the **Project Object Model** (POM) file. In it there is project meta data, dependencies which include  *starter* dependencies (packages of dependencies as one bundle), and project built tools.