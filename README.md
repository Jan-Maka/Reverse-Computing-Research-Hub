# Reverse-Computing-Research-Hub
Second Year Group Software Engineering Project that followed Agile/SCRUM.

User Stories I worked on:
-
- Search Engine
- Upload/View/Download Research Papers
- Calendar and Events Page
- Bug Fixes

## Technology stack.

- Language: Java 17
- Build tool : Gradle
- Framework: Spring Boot 3.0.2 <https://spring.io/projects/spring-boot>
- Template engine: Thymeleaf <https://www.thymeleaf.org>
- Frontend: HTML/CSS
  - HTML
  - CSS
  - Bootstrap 5 <https://getbootstrap.com/docs/5.0/getting-started/introduction/>
  - JQuery 3.6.3 <https://jquery.com>
  - Javasript
- Database: MySQL

***

# Development User Account Log-In Information

## Admin User: Mike Myers
- Email: mike@myers.com
- Password: password

## Standard User: Tony Stark
- Email: tony@mcu.com
- Password: password

## Running the Application
This Application is made using SpringMVC and a MySQL databse.

### Requisites
---
- Install Java 17+
- Install MySQL
- Google Search API Key

### Database Setup
---
The application requires a connection to an MySQL database as without it you won't be able to use the application.

#### Create Database
---
Create a databse that your willing to by changing {database} to the database name you want and the {username} and {password} to what you want.
```sql
CREATE DATABASE '{database}';
USE '{database}'
CREATE USER '{username}'@'localhost' IDENTIFIED BY '{password}';
GRANT ALL PRIVILEGES ON *.* TO '{username}'@'localhost';
QUIT;
```

#### Connect to Database
---
To connect the application with thedatabase you can replace the {database} with one you have created and the {username} and {password} for the databse in the application.properties file of the project (Located: [ResearchHubWepApp/src/main/resources](./ResearchHubWepApp/src/main/resources/application.properties)).

```yaml
# Database configuration
spring.datasource.url=jdbc:mysql://localhost:3306/{database}
spring.datasource.username={username}
spring.datasource.password={password}
```


### Deployment of Application
---
**Note it might take a minute for the application to fully start up due to dependicies needing to be configured.**

#### Deploy in IDE
---
If you have a Java Development Environment setup with IntelliJ and you configured the MySQL databse then you can simply load the project using IntelliJ.

#### Deploy Application on Windows
---
In your command line change the directory to the project root folder ([ResearchHubWepApp](./ResearchHubWepApp/)) and run the command.
```
gradlew.bat clean bootjar
```
Then change the directory to access the jar file and type the following which would start running the application on your device.
```
cd build\libs
java -jar ResearchHub-0.0.1-SNAPSHOT.jar
```
To see if it works go to your browser and vist <https://localhost:8443/login> to arrive at the login page.

#### Deploy Application on Linux and macOS
---
In your command line change the directory to the project root folder ([ResearchHubWepApp](./ResearchHubWepApp/)) and run the command.
```
./gradlew clean bootJar
```
Then change the directly to access the jar file and type the following which would start running th application on your device.

```
cd build/libs
java -jar ResearchHub-0.0.1-SNAPSHOT.jar
```
To see if it works go to your browser and vist <https://localhost:8443/login> to arrive at the login page.