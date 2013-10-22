scape-parent-pom
================

## Introduction
A parent pom.xml to be used by all SCAPE project Maven projects. The need for this arose when the time came to apply
a consistent license header across the Java projects using a
[Maven License Plugin](http://code.mycila.com/license-maven-plugin/), which could have meant cutting and pasting of a lot
of common information between the projects.

## Usage
In order to use the information in the parent file your Maven pom.xml must inherit from the pom in this project.
This is done by adding this xml fragment:
```
	<parent>
		<groupId>eu.scape-project</groupId>
		<artifactId>scape-parent</artifactId>
		<version>1.0.0</version>
	</parent>
```
to your projects top level pom.xml.  Your top level pom.xml may already inherit from a parent pom, for example:
```
  <parent>
    <groupId>org.sonatype.oss</groupId>
    <artifactId>oss-parent</artifactId>
    <version>7</version>
  </parent>
```
Indeed all SCAPE projects should previously have used this as a parent pom.  Using the new SCAPE pom.xml won't affect any
project that inherits from the sonatype pom, as it inherits from this pom itself.

## Further Reading
If you're interested in why we're recommending this, it's to stay in line with sonatypes [Maven Central publishing guide]
(https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide#SonatypeOSSMavenRepositoryUsageGuide-7a.1.POMandsettingsconfig).

The Apache Maven Introduction says a little about the [Maven inheritance model](http://maven.apache.org/guides/introduction/introduction-to-the-pom.html#Project_Inheritance).



 
