# Use Node.js LTS slim image
FROM node:20-bullseye-slim

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install --production

# Copy all source files
COPY . .

# Expose backend port
EXPOSE 4000

# Start Node using compiled JS
CMD ["node", "src/index.js"]
