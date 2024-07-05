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

# Build the React app
RUN npm run build

# Install a simple HTTP server to serve the static files
RUN npm install -g serve

# Expose the port the app runs on
EXPOSE 3000

# Command to run the app
CMD ["serve", "-s", "build"]
