# SpringBoot-Endpoints-AppEngineFlex
Integrate Cloud Endpoints with Spring Boot (Running on App Engine Flex)


This service given an Swagger 2.0 endpoint interface to manage Sprign boot Hello App in App Engine Flex environment.

Service is hosted at URL = https://qqqqq-xxx.appspot.com/

It is developed in springBoot, Java 8 runtime and is deployed on Google App Engine Flexible env.

Steps to Configure the Running app- 

Step 1 - Deploy Open API configuration(Swagger File) on Service Management(GCP).
Step 2 - Deploy the Spring Boot Api code on the App Engine Flex Environment.
Step 3 - See the graphs and monitoring page for the App enigne Flex App.


Step 1 - see the code openapi-appengine.yaml file above and how to deploy - 

        gcloud endpoints services deploy openapi-appengine.yaml
        
Step 2 - Update the pom.xml according to the above file, and deploy the code first local tomcat server  to check whether the Spring Boot app is working fine or not via below command -
                   
          mvn spring-boot:run
          
        Visit http://localhost:8080 for check the greet message.
        
Step 3 - Now Deploy the code on App Engine Flex via the cmd - 

         mvn appengine:deploy

Test the app -- 


Hit the https://qqqqq-xxx.appspot.com/hello on browser or copy the openapi-appengine.yaml file over swahher tool and test it. It will give you Hello World! 
