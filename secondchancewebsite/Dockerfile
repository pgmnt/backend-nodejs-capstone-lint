# Use Node.js 18 LTS (recommended for Express 5)
FROM node:18-slim

# Set working directory inside container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy everything else (including build folder)
COPY . .

# Expose port 9000
EXPOSE 9000

# Start the Express server
CMD ["node", "index.js"]