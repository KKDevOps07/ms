# Step 1: Use Node.js as the base image
FROM node:8

# Step 2: Set the working directory in the container
WORKDIR /app

# Step 4: Install dependencies
RUN npm install

# Step 5: Copy the rest of the application source code to the container
COPY . .

# Step 6: Build the React application
RUN npm run build

# Step 9: Expose the default Nginx port
EXPOSE 8080

# Step 10: Start Nginx
CMD ["npm", "start"]
