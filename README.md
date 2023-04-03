# RecipeMaster - Spring Boot Application to retrieve and store recipe details to database 

## Overview 

This Spring Boot application provides a restful API to retrieve the stored Recipe and allow user to add new Recipe. 
This also provides REST API to search recipes based on title and recipe categories 
This application can deployed easily and stores data in MYSQL database

## Prerequisites

-java Development Kit (JDK) 17 or higher
-Apache Maven 4.0.0 or higher
-Docker to connect mysql:8-oracle image or higher

### Running the Application
To run the application need to create a docker image of mysql DB using the following command : 

docker run --name recipe-master-mysql -p 51877 -e MYSQL_ROOT_PASSWORD={password} -d mysql:8-oracle

This will create a docker image name recipe-master-mysql and create a Database name mysql

Build and run the application using the following command : 

mvn clean install 
java -jar /target/recipemaster-0.0.1-SNAPSHOT.jar

The application will start on port 8080

### API Documentation 
Swagger documentation has been created for the RestAPI , which is available at :
http://localhost:8080/swagger-ui/index.html

Following REST API endpoints are being hosted 




