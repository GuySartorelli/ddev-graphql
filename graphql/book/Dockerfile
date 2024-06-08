# Use the official Node.js image as the base image
FROM node:20-alpine

# Install necessary packages
RUN apk update && apk add --no-cache ca-certificates bash

# Set the working directory
WORKDIR /app

# Copy all files to the container
COPY . .
RUN npm install && npm run build

# Expose the port the app runs on
EXPOSE 4000

# Define the command to run the application
CMD ["node", "dist/index.js"]
