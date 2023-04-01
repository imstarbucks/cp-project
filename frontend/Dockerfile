# Use an official Node runtime as a parent image
FROM node:14.18.0-alpine3.14

# Set the working directory to /frontend
WORKDIR /app

# Copy the current directory contents into the container at /frontend
COPY . /app

# Copy package.json and package-lock.json separately to leverage Docker caching
COPY package.json ./
COPY package-lock.json ./

# Install any needed packages
RUN npm install

# Make port 3000 available to the world outside this container
EXPOSE 3000

# Define environment variable for the API endpoint
ENV REACT_APP_API_ENDPOINT http://localhost:8000

# Run the command to start the server
CMD ["npm", "run", "dev"]
