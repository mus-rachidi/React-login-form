# Use an official Node.js runtime as the base image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application source code to the container
COPY . .

# Expose the port that your application will run on (3080, based on your provided code)
EXPOSE 3080

# Command to start the application (modify as needed)
CMD [ "node", "app.js" ]

