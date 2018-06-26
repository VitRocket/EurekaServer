# EurekaServer
Service Registration and Discovery

http://localhost:9000/
login: system
password: system

# Clients
https://github.com/VitRocket/SoapService
https://github.com/VitRocket/ClientService

# Run
mvn spring-boot:run

# Package
mvn package

# View
jar tvf EurekaServer-1.0-SNAPSHOT.jar

# Run
java -jar EurekaServer-1.0-SNAPSHOT.jar

# Docker
### 1 Create Dockerfile

    FROM java:8
    MAINTAINER user "user@example.com"
    COPY EurekaServer.jar /opt
    ENTRYPOINT ["/usr/bin/java", "-jar"]
    CMD ["/opt/EurekaServer.jar", "--server.port=8080"]
    
### 2 Commands
    sudo docker build -t eurekaserver .
#####
    sudo docker images
#####
    sudo docker run -p 8080:8080 -d eurekaserver
#####
    sudo docker ps -a
#####
    sudo docker stop elastic_leavitt
