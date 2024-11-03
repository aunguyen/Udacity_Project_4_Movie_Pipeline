# Use a Node.js base image
FROM public.ecr.aws/docker/library/node:18.14.2-alpine3.17

# Set the working directory inside the container to the current directory
WORKDIR /frontend

# Copy only the package.json and package-lock.json to install dependencies first (for caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose the port the app runs on
EXPOSE 3000

# Command to start the app
CMD ["npm", "start"]