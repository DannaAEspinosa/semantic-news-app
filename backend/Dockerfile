# Use the official Node.js image as the base
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the entire project into the container
COPY . .

# Build the NestJS project
RUN npm run build

# Expose the port your NestJS app runs on
EXPOSE 3000

# Start the production server
CMD ["node", "dist/main"]
