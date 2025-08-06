# Use an official Node.js runtime as a parent image
FROM node:21

# Set working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json separately to leverage Docker layer caching
COPY . .

# Install dependencies (production only, remove devDependencies optionally)
RUN npm i 

# Copy all app source code into the image
COPY .env.sample .env 

# Expose the port your backend server listens on (commonly 3000 or 5000, change if needed)
EXPOSE 5000

# Start the backend server
CMD ["npm", "start"]

