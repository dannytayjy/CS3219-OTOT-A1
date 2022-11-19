# Pull the latest LTS version 16 of Node image from Docker Hub
FROM node:16.18.1

# Create the app directory inside the container
WORKDIR /app

# Copy the package.json files from local machine to workdir in container
# A wildcard is used to ensure both package.json AND package-lock.json are
# copied where available (npm@5+)
COPY package*.json ./

# Run npm install in local machine
RUN npm install

# If you are building your code for production
# RUN npm ci --only=production

# Copy the generated modules and all other files to the container
COPY . .

# Expose port 8080 as the app is running on port 8080 inside the container
EXPOSE 8080

# Define the command that runs the app when the container is started
CMD [ "node", "index.js" ]
