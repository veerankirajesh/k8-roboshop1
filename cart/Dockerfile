# Use Node.js official image
FROM node:18.19.1-alpine3.19

# Expose port
EXPOSE 8080

# Create a user and group
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop

# Set working directory
WORKDIR /opt/server

# Give ownership to roboshop user
RUN chown roboshop:roboshop /opt/server

# Switch to non-root user
USER roboshop

# Copy package.json first (for caching npm install)
COPY package.json /opt/server/

# Copy the app code
COPY server.js /opt/server/

# Install dependencies
RUN npm install

# Start the application
CMD ["node", "server.js"]
