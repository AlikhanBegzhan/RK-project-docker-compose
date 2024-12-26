# Use a lightweight JDK image
FROM eclipse-temurin:8-jre

# Set the working directory inside the container
WORKDIR /app

# Copy the JAR file into the container
COPY build/libs/endterm-0.0.1-SNAPSHOT.jar /app/application.jar

# Expose the application port
EXPOSE 8081

# Set JVM memory limits for Java 8
# -Xms256m: Initial heap size of 256Mi
# -Xmx512m: Maximum heap size of 512Mi
ENTRYPOINT ["java", "-Xms256m", "-Xmx512m", "-jar", "/app/application.jar"]
