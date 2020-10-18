
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>demo.main</groupId>
  <artifactId>demo-1</artifactId>
  <packaging>war</packaging>
  <version>0.0.1-SNAPSHOT</version>
  <name>demo-1 Maven Webapp</name>
  <url>http://maven.apache.org</url>
  <!-- Specifying the Versions of Spring, Hibernate, MySQL etc -->
       <properties>
        <spring.version>5.2.8.RELEASE</spring.version>
        <hibernate.version>5.3.7.Final</hibernate.version>
        <mysql.version>8.0.16</mysql.version>
        <junit-version>4.12</junit-version>
        <servlet-api-version>3.0.1</servlet-api-version>
        <jsp-version>2.1</jsp-version>
        <jstl-version>1.2</jstl-version>
        
    </properties>
  
  <dependencies>
  
 <dependency>
    <groupId>org.mariadb.jdbc</groupId>
    <artifactId>mariadb-java-client</artifactId>
    <version>2.7.0</version>
</dependency>
  
  	<dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-core</artifactId>
            <version>${spring.version}</version>
        </dependency>
  
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-context</artifactId>
            <version>${spring.version}</version>
        </dependency>
  
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-web</artifactId>
            <version>${spring.version}</version>
        </dependency>
  
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-webmvc</artifactId>
            <version>${spring.version}</version>
        </dependency>
  
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-orm</artifactId>
            <version>${spring.version}</version>
        </dependency>
  
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-test</artifactId>
            <version>${spring.version}</version>
            <scope>test</scope>
        </dependency>
       
       <!-- Hibernate 4 dependencies -->
        <dependency>
            <groupId>org.hibernate</groupId>
            <artifactId>hibernate-core</artifactId>
            <version>${hibernate.version}</version>
        </dependency>
        	
        <dependency>
            <groupId>org.hibernate</groupId>
            <artifactId>hibernate-c3p0</artifactId>
            <version>${hibernate.version}</version>
        </dependency>
        
        <!--MYSQL Connector -->
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>${mysql.version}</version>
        </dependency>
  
        <!-- Servlet and JSP -->
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>javax.servlet-api</artifactId>
            <version>${servlet-api-version}</version>
        </dependency>
  
        <dependency>
            <groupId>javax.servlet.jsp</groupId>
            <artifactId>jsp-api</artifactId>
            <version>${jsp-version}</version>
            <scope>provided</scope>
        </dependency>
  
        <!-- JSTL dependency -->
        <dependency>
            <groupId>jstl</groupId>
            <artifactId>jstl</artifactId>
            <version>${jstl-version}</version>
        </dependency>
  
        <!-- JUnit -->
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>${junit-version}</version>
      <scope>test</scope>
    </dependency>
    
    <!-- https://mvnrepository.com/artifact/taglibs/standard -->
	<dependency>
    	<groupId>taglibs</groupId>
    	<artifactId>standard</artifactId>
    	<version>1.1.2</version>
	</dependency>   
    
  </dependencies>
  <build>
    <finalName>demo-1</finalName>
    <plugins>
              <plugin>
                <artifactId>maven-surefire-plugin</artifactId>
                <configuration>
                    <includes>
                        <include>**/*Tests.java</include>
                    </includes>
                </configuration>
            </plugin>
            <plugin>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.7.0</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
  </build>
</project>
