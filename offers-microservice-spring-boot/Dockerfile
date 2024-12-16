# Use an official Maven image as the base
FROM maven as build

# Set the working directory inside the container
WORKDIR /app

# Copy the Maven project's POM file and source code into the container
COPY . .

RUN mvn install

# Final stage: Create a lightweight image to run the Java application
FROM openjdk:11.0.10-jre

# Set the working directory
WORKDIR /app

# Copy the built JAR file from the builder stage to the final image
COPY --from=build /app/target/offers-0.0.1-SNAPSHOT.jar /app

# Expose the port your app runs on
EXPOSE 1001

# Define the command to run your applic
CMD ["java", "-jar", "offers-0.0.1-SNAPSHOT.jar"]
