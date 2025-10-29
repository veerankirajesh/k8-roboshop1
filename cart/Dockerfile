FROM node:18.19.1-alpine3.19

# Set working directory
WORKDIR /opt/server

# Create non-root user
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
RUN chown roboshop:roboshop /opt/server
USER roboshop

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy all source files
COPY . .

# Expose application port
EXPOSE 8080

# Start the Node app
CMD ["node", "service.js"]
