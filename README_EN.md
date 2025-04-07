[中文](README.md) | [English](README_EN.md)

<p align="center">
  <a href="https://github.com/pangju666/java-pangju-dependencies/releases">
    <img alt="GitHub release" src="https://img.shields.io/github/release/pangju666/java-pangju-dependencies.svg?style=flat-square&include_prereleases" />
  </a>

  <a href="https://central.sonatype.com/search?q=g:io.github.pangju666%20%20a:pangju-dependencies&smo=true">
    <img alt="maven" src="https://img.shields.io/maven-central/v/io.github.pangju666/pangju-dependencies.svg?style=flat-square">
  </a>

  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img alt="code style" src="https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square">
  </a>
</p>

# Introduction

Maven dependency management project, this project inherits from spring-boot-dependencies.

```xml

<parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-dependencies</artifactId>
    <version>Latest Version</version>
    <relativePath/> <!-- lookup parent from repository -->
</parent>
```

# Usage

This dependency management package can be defined as a project parent using the parent tag approach.

```xml
<parent>
    <groupId>io.github.pangju666</groupId>
    <artifactId>pangju-dependencies</artifactId>
    <version>Latest Version</version>
    <relativePath/> <!-- lookup parent from repository -->
</parent>
```

Or use the dependencyManagement tag to import this dependency management package into the project.

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>io.github.pangju666</groupId>
            <artifactId>pangju-dependencies</artifactId>
            <version>Latest Version</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## License

Pangju Dependencies is Open Source software released under
the [Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0.html).