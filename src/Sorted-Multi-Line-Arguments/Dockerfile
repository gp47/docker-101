# Use a minimal base image
FROM node:14-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies (sorted alphabetically)
COPY package.json package-lock.json ./
RUN npm install --production && rm -rf /tmp/*

# Copy application code
COPY . .

# Install system dependencies (sorted alphabetically)
RUN apk add --no-cache \
    bash \
    curl \
    git \
    openssl \
    python3

# Expose the necessary port
EXPOSE 3000

# Start the application
CMD ["node", "server.js"]
