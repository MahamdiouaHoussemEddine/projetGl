FROM node:20.17.0

# Set the working directory
WORKDIR /app

# Copy the package.json and package-lock.json files from your host to your current location in the container
COPY package*.json ./

# Install the dependencies defined in package.json
RUN npm install

# Rebuild bcrypt for the correct architecture
RUN npm rebuild bcrypt --build-from-source

# Copy the rest of your app's source code from your host to your image filesystem
COPY . .

# Inform Docker that the container is listening on port 3000 at runtime
EXPOSE 3000

# Run the specified command within the container to start the application
CMD ["npm", "run", "dev"]