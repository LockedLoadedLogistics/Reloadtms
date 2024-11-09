# Use an appropriate Node.js version
FROM node:16

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Clean npm cache and install dependencies
RUN npm cache clean --force
RUN npm install --no-audit --progress=false

# Copy the rest of your application code
COPY . .

# Build the application
RUN npm run build

# Expose the port (80 for internal, change if needed)
EXPOSE 80

# Command to run your application
CMD ["npm", "start"]
