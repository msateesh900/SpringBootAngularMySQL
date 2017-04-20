# SpringBootAngularMySQL Application

#### Following technologies stack being used:
```
1.Spring Boot 1.4.3.RELEASE
2.Spring 4.3.5.RELEASE [transitively]
3.Spring data JPA 1.10.6.RELEASE [transitively]
4.Hibernate 5.0.11.Final [transitively]
5.MySQL 5.1.40 [transitively]
6.H2 1.4.187
7.Hikari CP 2.4.7 [transitively]
8.AngularJS 1.5.8
9.Maven 3.1
10.JDK 1.8
11.Eclipse or STS
```

Create Database websystique and execute the query as follows:
```
Create Database websystique;
use websystique;
create table APP_USER (
   id BIGINT NOT NULL AUTO_INCREMENT,
   name VARCHAR(30) NOT NULL,
   age  INTEGER NOT NULL,
   salary REAL NOT NULL,
   PRIMARY KEY (id)
);
   
INSERT INTO APP_USER(name,age,salary)
VALUES ('sateesh',26,80000);
   
INSERT INTO APP_USER(name,age,salary)
VALUES ('Satya',40,50000);
 
commit;
```
This application will run in two profiles
```
1.local
2.produ
Run in local(H2 DB)       ----------> java -jar target/SpringBootCRUDApplicationExample-1.0.0.jar --spring.profiles.active=local
Run in production (MYSQL) ----------> java -jar target/SpringBootCRUDApplicationExample-1.0.0.jar --spring.profiles.active=prod
```

Build and Run Application using maven as follows:
```
$ mvn clean install
$ mvn spring-boot:run
```
