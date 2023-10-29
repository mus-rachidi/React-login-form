# Use an official Node.js runtime with Alpine Linux as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json to the container
COPY package*.json ./

# Install the project dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the React app for production
RUN npm run build

# Expose the port on which your app runs (default is 3000)
EXPOSE 3000

# Command to run your React app
CMD ["npm", "start"]

