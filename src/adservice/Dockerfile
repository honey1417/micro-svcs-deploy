# Use a lightweight OpenJDK image
FROM openjdk:17-jdk-slim

# Create the required directory
RUN mkdir -p /adservice

# Download the JAR from Nexus repo
#this version the docker cont exited so wrote another docker file
ADD http://34.72.222.210:8081/repository/adservice/hipstershop/adservice/1.0-SNAPSHOT/adservice-1.0-20250318.154359-1.jar  /adservice/adservice.jar

# Expose the port your app runs on (if applicable)
EXPOSE 8090

# Run the JAR
ENTRYPOINT ["java", "-jar", "/adservice/adservice.jar"]

