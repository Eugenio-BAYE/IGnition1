# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /home/ubuntu/IGnition

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Bundle app source
COPY . .

# Build the React application
RUN npm run build

# Install serve to serve static files on production
RUN npm install -g serve

# Expose the port app runs on
EXPOSE 3000

# Define the command to run your app
CMD ["serve", "-s", "build", "-l", "3000"]

