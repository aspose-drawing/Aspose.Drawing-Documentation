---
title: "Installation"
type: docs
url: /java/installation/
weight: 50
keywords: Java installation, Maven repository, Maven project, Aspose dependency, pom.xml
description: Learn about Aspose.Drawing for Java installation through Maven repository and dependency definition in pom.xml Maven project file.
---

## **Installing Aspose.Drawing for Java through Maven**

<a href="https://repository.aspose.com/repo/com/aspose/">Maven repository</a> hosted by Aspose is the easiest way to download and install Aspose APIs for Java. You can use your Maven Project configuration to specify the repository configuration. Add Aspose Maven repository in your Maven `pom.xml` file: 

```xml
 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://repository.aspose.com/repo/</url>
    </repository>
</repositories>
```

Define the following dependency for Aspose.Drawing Java in your `pom.xml` file:

```xml
 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-drawing</artifactId>
        <version>23.10</version>
        <classifier>jdk16</classifier>
   </dependency>

   <!-- if you need a documentation, please add the following dependency. For example it could be useful for IDE. -->
   <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-drawing</artifactId>
        <version>23.10</version>
        <classifier>javadoc</classifier>
   </dependency>
</dependencies>
```

Aspose.Drawing for Java dependency is defined in your Maven project after finishing these steps.
