scape-setup
================

## Introduction
This repository is a home for SCAPE related files that are used with other projects.
Currently there are two items in the repo, the [README.template](README.template) and the [SCAPE Parent POM](pom.xml).

## README Template
The README template prescribes the information that the SCAPE project would like to see in ALL project README.md files.
These are the first point of contact with a GitHub project for most users and should contain as much useful information
as possible.

### Usage
Copy the README.template file from this project into the root directory of a new project as README.md, then fill in the
details as best you can. Please don't delete fields that you can't fill in UNLESS YOU'RE SURE that they don't apply to
your project. For any fields that can be filled in at a later date, simply add a TODO marker with a brief statement of
when this might will be done, this doesn't have to be a specific date but instead can state what is required before the
field can be completed.  For example the download area could be filled in as:
```
TODO: Add download link when initial prototype release is ready.
```

### More About READMEs
GitHub README.md files are created using [GitHub flavoured markdown](https://help.github.com/articles/github-flavored-markdown).

## Parent POM
A parent pom.xml to be used by all SCAPE project Maven projects. The need for this arose when the time came to apply
a consistent license header across the Java projects using a
[Maven License Plugin](http://code.mycila.com/license-maven-plugin/), which could have meant cutting and pasting of a lot
of common information between the projects.

### Usage
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

### More About Parent POMS
If you're interested in why we're recommending this, it's to stay in line with sonatypes [Maven Central publishing guide]
(https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide#SonatypeOSSMavenRepositoryUsageGuide-7a.1.POMandsettingsconfig).

The Apache Maven Introduction says a little about the [Maven inheritance model](http://maven.apache.org/guides/introduction/introduction-to-the-pom.html#Project_Inheritance).



 
