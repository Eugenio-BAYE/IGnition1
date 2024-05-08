# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /home/ubuntu/IGnition/back/

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Bundle app source
COPY . .

# Expose port to access the server
EXPOSE 5000

# Define the command to run your app using CMD which defines your runtime
CMD ["node", "app.js"]

