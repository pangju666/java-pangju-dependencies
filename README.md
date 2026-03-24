<p align="center">
  <a href="https://github.com/pangju666/java-pangju-dependencies/releases">
    <img alt="GitHub release" src="https://img.shields.io/github/release/pangju666/java-pangju-dependencies.svg?style=flat-square&include_prereleases" />
  </a>

  <a href="https://central.sonatype.com/search?q=g:io.github.pangju666%20a:pangju-dependencies&smo=true">
    <img alt="maven" src="https://img.shields.io/maven-central/v/io.github.pangju666/pangju-dependencies.svg?style=flat-square">
  </a>

  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img alt="license" src="https://img.shields.io/badge/license-Apache%202-4EB1BA.svg?style=flat-square">
  </a>

  <img alt="JDK" src="https://img.shields.io/badge/JDK-17+-blue.svg?style=flat-square">
</p>

# Pangju Dependencies

`Pangju Dependencies` 是一个基于 `Spring Boot Dependencies` 的依赖与插件版本统一管理项目（BOM）。它旨在为各类 Java
项目提供一套经过验证的、开箱即用的三方库版本组合，简化依赖配置，提升项目一致性，避免版本冲突。

## 🌟 核心特性

- **广泛适用性**: 虽基于 `Spring Boot Dependencies` 构建，但其管理的版本库适用于所有 Java 项目，并非仅限于 Spring Boot 应用。
- **精选第三方库**: 涵盖了常用的工具库、数据库增强、安全框架、中间件客户端等。
- **插件化管理**: 预设了常用的 Maven 插件配置（如 Javadoc、Source、GPG 等），提升构建效率。
- **版本一致性**: 通过 BOM (Bill of Materials) 机制，确保多模块项目中的依赖版本严格一致。

## 📦 管理的主要组件

本项目管理了包括但不限于以下常用组件的版本：

- **数据库/持久层**: MyBatis Plus, Dynamic Datasource, P6Spy, Redisson
- **安全/鉴权**: Sa-Token, Java JWT, Jasypt
- **文档/报表**: Apache POI, POI-tl, Apache Tika, PDFBox, Fastexcel
- **工具类**: Guava, Commons 系列, MapStruct, Thumbnailator, Jsoup
- **其他**: Resilience4j, Spock Framework, HanLP, BoofCV

## 📖 文档

更详细的使用说明和 API
文档请参考：[在线文档](https://pangju666.github.io/pangju-java-doc/dependencies/getting-started.html)

## 🚀 快速开始

### 环境要求

- **JDK**: 17+
- **Maven**: 3.6.3+

### 1. 作为父 POM 使用（推荐）

适用于新项目，可以直接继承本项目的基础配置。

```xml
<parent>
    <groupId>io.github.pangju666</groupId>
    <artifactId>pangju-dependencies</artifactId>
    <version>1.1.0</version>
    <relativePath/>
</parent>
```

### 2. 作为 BOM 导入

适用于已有父 POM 或需要灵活组合的场景。

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>io.github.pangju666</groupId>
            <artifactId>pangju-dependencies</artifactId>
            <version>1.1.0</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

### 3. 使用受管依赖

在子项目中引入依赖时，无需指定版本号。

```xml
<dependencies>
    <!-- MyBatis Plus 示例 -->
    <dependency>
        <groupId>com.baomidou</groupId>
        <artifactId>mybatis-plus-spring-boot3-starter</artifactId>
    </dependency>
    <!-- Sa-Token 示例 -->
    <dependency>
        <groupId>cn.dev33</groupId>
        <artifactId>sa-token-spring-boot3-starter</artifactId>
    </dependency>
    <!-- 工具库示例 -->
    <dependency>
        <groupId>com.google.guava</groupId>
        <artifactId>guava</artifactId>
    </dependency>
</dependencies>
```

## 📄 许可证

本项目采用 [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) 许可证。

---
感谢所有为项目做出贡献的开发者，以及项目所使用的开源框架和工具。
