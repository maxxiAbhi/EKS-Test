# Use the official Node.js LTS image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install PM2 globally
RUN npm install -g pm2

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the full app source
COPY . .

# Expose the port your app listens on
EXPOSE 3001

# Use PM2 to run `npm start`
CMD ["pm2-runtime", "npm", "--", "start"]