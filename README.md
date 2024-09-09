Gatling Java API Udemy Course Code
============================================
* run in the terminal: .\mvnw.cmd gatling:test

* add in the pom.xml file:
      <configuration>
        <runMultipleSimulations>true</runMultipleSimulations>
      </configuration>

         
* the working full pom file:
---------------------------------------------------------
    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">

      <modelVersion>4.0.0</modelVersion>

      <groupId>io.gatling.demo</groupId>
      <artifactId>gatling-java-api</artifactId>
      <version>3.8.3</version>

      <properties>
        <!-- use the following if you're compiling with JDK 8-->
    <!--    <maven.compiler.source>1.8</maven.compiler.source>-->
    <!--    <maven.compiler.target>1.8</maven.compiler.target>-->
        <!-- comment the 2 lines above and uncomment the line bellow if you're compiling with JDK 11 or 17 -->
            <maven.compiler.release>17</maven.compiler.release>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <gatling.version>${project.version}</gatling.version>
        <gatling-maven-plugin.version>4.2.6</gatling-maven-plugin.version>
        <maven-compiler-plugin.version>3.10.1</maven-compiler-plugin.version>
        <maven-jar-plugin.version>3.2.2</maven-jar-plugin.version>
      </properties>

      <dependencies>
        <dependency>
          <groupId>io.gatling.highcharts</groupId>
          <artifactId>gatling-charts-highcharts</artifactId>
          <version>${gatling.version}</version>
          <scope>test</scope>
        </dependency>

        <dependency>
          <groupId>org.apache.commons</groupId>
          <artifactId>commons-lang3</artifactId>
          <version>3.12.0</version>
        </dependency>
      </dependencies>

      <build>
        <plugins>
          <plugin>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>${maven-compiler-plugin.version}</version>
          </plugin>
          <plugin>
            <artifactId>maven-jar-plugin</artifactId>
            <version>${maven-jar-plugin.version}</version>
          </plugin>
          <plugin>
            <groupId>io.gatling</groupId>
            <artifactId>gatling-maven-plugin</artifactId>
            <version>${gatling-maven-plugin.version}</version>
            <configuration>
              <runMultipleSimulations>true</runMultipleSimulations>
            </configuration>


          </plugin>
        </plugins>
      </build>
    </project>

    ---------------------------------------------------------

