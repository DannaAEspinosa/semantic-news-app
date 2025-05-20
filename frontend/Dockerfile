# Use Node.js as the base image
FROM node:18-alpine

# Set the working directory
WORKDIR /app

# Copy dependency files first to optimize Docker cache
COPY package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the rest of the project files
COPY . .

# Build the Next.js frontend
RUN npm run build

# Expose the port Next.js uses in production
EXPOSE 3000

# Start the production server
CMD ["npm", "start"]
