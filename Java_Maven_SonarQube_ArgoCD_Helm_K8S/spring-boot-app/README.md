## Spring Boot Java Web Application
This repository contains a Spring Boot-based Java web application built using Maven. The application follows the MVC architecture, where the controller sends a response containing title and message attributes to the view.

## Running the Application Locally
1. Clone the Repository
Download the source code and navigate to the project directory:

      git clone https://github.com/SathwikaKarre/CI-CD-Pipeline-Automation/Java_maven_sonarqube_argocd_helm_k8s/spring-boot-app
   
      cd java-maven-sonar-argocd-helm-k8s/sprint-boot-app
   
3. Build the Application
Use Maven to compile and package the project:

      mvn clean package
   
After a successful build, the generated artifact can be found in the target/ directory.

## Running the Application

Option 1: Run Locally (Requires Java 11)

Execute the JAR file to start the application:

    java -jar target/spring-boot-web.jar
    
The application will be accessible at:

    http://localhost:8080

Option 2: Run as a Docker Container

1. Build the Docker Image
   
    docker build -t my-spring-boot-app:v1 .
   
2. Run the Container
   
    docker run -d -p 8010:8080 my-spring-boot-app:v1
   
The application can now be accessed at:

    http://<your-ip>:8010

Setting Up SonarQube Locally
    To analyze the code quality, SonarQube can be set up on your system. Follow these steps:
    
        apt install unzip
        
adduser sonaruser
      wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
      
      unzip sonarqube-9.4.0.54424.zip
      
      chmod -R 755 /home/sonaruser/sonarqube-9.4.0.54424
      
      chown -R sonaruser:sonaruser /home/sonaruser/sonarqube-9.4.0.54424
      
      cd sonarqube-9.4.0.54424/bin/linux-x86-64/
      
      ./sonar.sh start
      
Once started, SonarQube will be available at:
      http://<your-ip>:9000

## Next Steps

    Integrate SonarQube with Jenkins for automated static code analysis.
    
    Deploy the application on Kubernetes using Helm.
    
    Use Argo CD to manage production deployments.
    
    This project provides a foundation for implementing continuous integration and continuous deployment (CI/CD) for a Spring Boot-based Java web application.
    
    
    
    
    
    
    
    
    
    
    
    
    
