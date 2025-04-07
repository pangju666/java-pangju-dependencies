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

# 介绍

maven依赖管理项目，此项目继承自spring-boot-dependencies

```xml

<parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-dependencies</artifactId>
    <version>Latest Version</version>
    <relativePath/> <!-- lookup parent from repository -->
</parent>
```

# 使用方法

可以使用parent标签的方式将这个依赖管理包定义为项目父级依赖
```xml
<parent>
    <groupId>io.github.pangju666</groupId>
    <artifactId>pangju-dependencies</artifactId>
    <version>Latest Version</version>
    <relativePath/> <!-- lookup parent from repository -->
</parent>
```

或者使用dependencyManagement标签将这个依赖管理包导入到项目里
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

## 相关链接

- [文档](https://juejin.cn/post/7478893732191535142)

## 开源协议

本项目基于 [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0.html) 协议开源.