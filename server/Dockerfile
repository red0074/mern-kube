# Use the official Node.js image
FROM node:16

# Create and set the working directory
WORKDIR /app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the server runs on
EXPOSE 3001

# Command to run the server
CMD ["node", "server.js"]
