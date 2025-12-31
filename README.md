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
</p>

# Pangju Dependencies

## 简介

Pangju Dependencies 是一个基于 Spring Boot 官方父 POM（spring-boot-starter-parent）扩展的依赖与插件版本统一管理工程。
通过集中化的 dependencyManagement 与 pluginManagement，帮助项目：

- 统一三方库版本，避免冲突与“传染性”升级问题
- 引入常用 BOM 并管理多模块依赖的版本
- 固化常用插件版本与基础配置，提升构建稳定性

## 快速开始

1. 作为父 POM 使用（推荐）

```xml
<parent>
    <groupId>io.github.pangju666</groupId>
    <artifactId>pangju-dependencies</artifactId>
    <version>最新版本</version>
    <relativePath/> <!-- 可保持为空以从仓库解析 -->
</parent>
```

2. 作为 BOM 导入（适用于已有父 POM 的场景）

```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>io.github.pangju666</groupId>
            <artifactId>pangju-dependencies</artifactId>
            <version>最新版本</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

3. 添加三方依赖（无需显式声明版本）

```xml

<dependencies>
    <!-- 示例：受统一版本管理的依赖 -->
    <dependency>
        <groupId>org.apache.poi</groupId>
        <artifactId>poi</artifactId>
    </dependency>
    <dependency>
        <groupId>org.redisson</groupId>
        <artifactId>redisson-spring-boot-starter</artifactId>
    </dependency>
    <dependency>
        <groupId>net.coobird</groupId>
        <artifactId>thumbnailator</artifactId>
    </dependency>
</dependencies>
```

4. 使用受管插件（在子工程显式声明插件，无需版本号）

```xml

<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-javadoc-plugin</artifactId>
            <!-- 版本由父工程 pluginManagement 管理 -->
        </plugin>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-source-plugin</artifactId>
        </plugin>
        <!-- 如需 GPG 签名，可按需配置 -->
        <!--<plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-gpg-plugin</artifactId>
            <configuration>
                <skip>true</skip>
            </configuration>
        </plugin>-->
    </plugins>
</build>
```

## 许可证

本项目采用 Apache License 2.0 许可证 - 详情请参阅 [LICENSE](file:///e:/project/pangju/pangju-dependencies/LICENSE) 文件。

## 致谢

感谢所有为项目做出贡献的开发者，以及项目所使用的开源框架和工具。
