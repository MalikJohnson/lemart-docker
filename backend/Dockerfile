# Use a slim OpenJDK image
FROM openjdk:21-jdk-slim

# Set working directory inside container
WORKDIR /app

# Copy the jar file into the container
COPY target/LeMart-0.0.1-SNAPSHOT.jar app.jar

# Command to run your app
ENTRYPOINT ["java", "-jar", "app.jar"]
