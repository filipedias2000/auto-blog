# FROM	Create a new build stage from a base image.
FROM node:20-bullseye-slim

# WORKDIR	Change working directory.
WORKDIR /app

# COPY	Copy files and directories.
COPY package*.json ./

# RUN	Execute build commands.
RUN npm install

COPY . .

# ✅ Build TypeScript
RUN npm run build

# EXPOSE	Describe which ports your application is listening on.
EXPOSE 4000

# CMD	Specify default commands.
CMD ["npm", "run", "start"]

# Will need the environment variables for the database
