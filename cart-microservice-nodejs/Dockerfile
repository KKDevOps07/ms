# Use an official Maven image as the base
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy the Maven project's POM file and source code into the container
COPY . .

RUN npm install

# Define the command to run your applic
CMD ["node", "index.js"]
EXPOSE 1004
