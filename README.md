# Flink1.13
自学flink，版本是1.13，视频地址：https://www.bilibili.com/video/BV133411s7Sa?from=search&seid=15166254677336163840&spm_id_from=333.337.0.0
<hr>

## 第一章 快速上手
### 1.1 环境准备
- Java 8
- IDEA开发工具
- 一定的Java基础

### 1.2 创建项目
1. 创建一个maven项目，名字自拟
2. 添加如下依赖
   ```xml
   <properties>
        <!-- flink版本 -->
        <flink.version>1.13.0</flink.version>
        <!-- java版本 -->
        <java.version>1.8</java.version>
        <!-- scala版本，Flink的架构中使用了 Akka 来实现底层的分布式通信，而 Akka 是用 Scala 开发的，因此要引入Scala -->
        <scala.binary.version>2.12</scala.binary.version>
        <!-- 日志版本-->
        <slf4j.version>1.7.30</slf4j.version>
   </properties>

   <dependencies>
       <dependency>
            <groupId>org.apache.flink</groupId>
            <artifactId>flink-java</artifactId>
            <version>${flink.version}</version>
       </dependency>

       <dependency>
            <groupId>org.apache.flink</groupId>
            <artifactId>flink-streaming-java_${scala.binary.version}</artifactId>
            <version>${flink.version}</version>
       </dependency>

       <dependency>
            <groupId>org.apache.flink</groupId>
            <artifactId>flink-clients_${scala.binary.version}</artifactId>
            <version>${flink.version}</version>
       </dependency>

       <!-- 引入日志管理相关依赖 -->
       <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-api</artifactId>
            <version>${slf4j.version}</version>
       </dependency>

       <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-log4j12</artifactId>
            <version>${slf4j.version}</version>
       </dependency>

       <dependency>
            <groupId>org.apache.logging.log4j</groupId>
            <artifactId>log4j-to-slf4j</artifactId>
            <version>2.14.0</version>
       </dependency>
   </dependencies>
   ```
