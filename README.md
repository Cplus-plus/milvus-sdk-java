# Milvus Java SDK

[![Maven Central](https://img.shields.io/maven-central/v/io.milvus/milvus-sdk-java.svg)](https://search.maven.org/artifact/io.milvus/milvus-sdk-java/)

Java SDK for [Milvus](https://github.com/milvus-io/milvus). To contribute to this project, please read our [contribution guidelines](https://github.com/milvus-io/milvus/blob/master/CONTRIBUTING.md) first.

## Getting started

### Prerequisites

    -   Java 8 or higher
    -   Apache Maven or Gradle

The following table shows compatibilities between Milvus and Java SDK.

| Milvus version | Java SDK version |
|:--------------:|:----------------:|
|      2.0       |      2.0.4       |
|      2.1       |   2.1.0-beta4    |
| 2.2.0 ~ 2.2.8  |  2.2.0 ~ 2.2.5   |
|    >= 2.2.9    |  2.2.7 ~ 2.2.15  |
|     2.3.x      |      2.3.11      |
|     2.4.x      |      2.4.11      |
|     2.5.x      |      2.5.11      |
|     2.6.x      |      2.6.1       |

### Install Java SDK

You can use **Apache Maven** or **Gradle** add Milvus SDK to your project.

   - Apache Maven

       ```xml
        <dependency>
            <groupId>io.milvus</groupId>
            <artifactId>milvus-sdk-java</artifactId>
            <version>2.6.1</version>
        </dependency>
       ```

   - Gradle/Groovy

        ```groovy
        implementation 'io.milvus:milvus-sdk-java:2.6.1'
        ```

   - Gradle/Kotlin

        ```kotlin
        implementation("io.milvus:milvus-sdk-java:2.6.1")
        ```
  
From v2.5.2, milvus Java SDK is split into two packages: milvus-sdk-java and milvus-sdk-java-bulkwriter, because BulkWriter requires quite a lot of dependencies. If you don't need BulkWriter tool, you can ignore the milvus-sdk-java-bulkwriter package.
To use BulkWriter, import milvus-sdk-java-bulkwriter to your project.

   - Apache Maven

    ```xml
     <dependency>
         <groupId>io.milvus</groupId>
         <artifactId>milvus-sdk-java-bulkwriter</artifactId>
         <version>2.6.1</version>
     </dependency>
    ```

   - Gradle/Groovy

     ```groovy
     implementation 'io.milvus:milvus-sdk-java-bulkwriter:2.6.1'
     ```

   - Gradle/Kotlin

     ```kotlin
     implementation("io.milvus:milvus-sdk-java-bulkwriter:2.6.1")
     ```     

### Examples

Please refer to [examples](https://github.com/milvus-io/milvus-sdk-java/tree/master/examples) folder for Java SDK examples.

### Documentation



### Troubleshooting

- If you encounter the following error when running your application:
    ```
    Exception in thread "main" java.lang.NoClassDefFoundError: org/slf4j/LoggerFactory
    ```
  This is because SLF4J jar files need to be added into your application's classpath. SLF4J is required by Java SDK for logging purpose.
  
  To fix this issue, you can use **Apache Maven** or **Gradle** to download the required jar files.
                                                                                                         
    - Apache Maven
    
        ```xml
         <dependency>
             <groupId>org.slf4j</groupId>
             <artifactId>slf4j-api</artifactId>
             <version>1.7.30</version>
         </dependency>
        ```
    
    - Gradle/Groovy
    
         ```groovy
         compile group: 'org.slf4j', name: 'slf4j-api', version: '1.7.30'
         ```
    - Gradle/Kotlin
    
        ```kotlin
        implementation("org.slf4j:slf4j-api:1.7.30")
        ```

### Development

For developers interested in contributing to the Milvus Java SDK, please refer to our [DEVELOPMENT.md](DEVELOPMENT.md) file. This document provides detailed instructions on:

- Setting up your development environment
- Cloning the repository
- Building the SDK
- Updating Milvus proto files
- Running tests
- Contributing guidelines

We welcome contributions from the community!