---
layout: post
title:  "Multi-module Maven Project"
date:   2019-09-05 17:33:11 -0400
categories: blog
comments: true
---

Do you ever sometime find a project that needs to be broken into modules? Yeah, that's the `S` in SOLID, i.e., Single Responsibility Principle.
Fear not, there's Maven for that. Keep in mind, there are also other build tools than Maven that provides multi-module functionality. For this, I'll
choose to use Maven because it's easy for a small project. For a larger project, I'd recommend using Gradle.

To get started, you could follow the steps to create multi-module project.

1. Let's use Maven archetype and navigate into that folder: `mvn archetype:generate -DgroupId=com.jmsweb -DartifactId=multi-module
-DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false; cd multi-module`.
2. Open `multi-module/pom.xml` and edit the file to add `<packaging>pom</packaging>` after `<url>...</url>`. This will become the parent POM for modules
to build under.
3. Once inside multi-module directory, run the archetype command one more time to generate a JAR module:  `mvn archetype:generate -DgroupId=com.jmsweb
-DartifactId=child-module -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false; cd child-module`.
4. Open `child-module/pom.xml` and edit the file to add `<packaging>jar</packaging>` after `<url>...</url>`. This will become java JAR module to
to build.
5. The parent and child modules need to know about each other. Let's open the `child-module/pom.xml` and add the following snippet:<br/>
```xml
    <parent>
        <groupId>com.jmsweb</groupId>
        <artifactId>multi-module</artifactId>
        <version>0.0.1-SNAPSHOT</version>
    </parent>
```
6. The parent module need to know about its child modules. Let's open the `multi-module/pom.xml` and add the following snippet:<br/>
```xml
    <modules>
        <module>child-module</module>
    </modules>
```
7. If done correctly, you should be able to execute the command: `mvn clean install` in the multi-module directory. Maven will build the project and assemle
the code into a nice JAR file under `child-module/target/child-module.jar`.

I've done this so many times that I can literally do this in my sleep, from command line, or from IDE. My apologizes if I did not provide enough steps.
You can always get more information from [Apache Maven Project](https://maven.apache.org/guides/mini/guide-multiple-modules.html) website.