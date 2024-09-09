# Backend Dockerfile
FROM node:14-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install --production

# Copy the rest of the application code
COPY . .

# Expose the API port
EXPOSE 3000

# Start the Node.js API server
CMD ["node", "server.js"]
