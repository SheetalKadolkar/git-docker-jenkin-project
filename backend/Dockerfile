# Use Node.js LTS
FROM node:18

# Set working directory
WORKDIR /usr/src/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy backend code
COPY . .

# Expose port
EXPOSE 3000

# Start the server
CMD ["npm", "start"]
