# Use the official OpenJDK base image
FROM openjdk:17-jdk-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the built jar file into the container
COPY build/libs/curd-web-application-0.0.1-SNAPSHOT.jar /app/curd-web-application-0.0.1-SNAPSHOT.jar
# Expose port 8080
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "curd-web-application-0.0.1-SNAPSHOT.jar"]