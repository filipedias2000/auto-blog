# Use Node.js LTS slim image
FROM node:20-bullseye-slim

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./

# ✅ Install ALL dependencies including dev (Prisma needs this)
RUN npm install

# ✅ Explicitly copy Prisma schema
COPY prisma ./prisma

# Copy all source files
COPY . .

# Expose backend port
EXPOSE 4000

# Start Node using compiled JS
CMD ["node", "src/index.js"]
