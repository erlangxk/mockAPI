FROM node:22-alpine

# Create app directory
WORKDIR /app

# Copy package.json and package-lock.json files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy configuration and other files
COPY data.json ./
COPY .gitignore ./
COPY README.md ./

# Expose port 3000 for the Mockoon server
EXPOSE 3000

# Start the mock server
CMD ["npm", "start"]