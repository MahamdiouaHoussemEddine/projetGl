FROM node:20.17.0

# Set the working directory
WORKDIR /app

# Copy the package.json and package-lock.json files from your host to your current location in the container
COPY package*.json ./

# Install the dependencies defined in package.json
RUN npm install

# Inform Docker that the container is listening on port 5173 at runtime
EXPOSE 5173

# Copy the rest of your app's source code from your host to your image filesystem
COPY . .

# Run the specified command within the container to start the application
CMD ["npm", "run", "dev"]