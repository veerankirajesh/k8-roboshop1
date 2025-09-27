FROM node:18.19.1-alpine3.19
EXPOSE 8080

# Create user
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop

WORKDIR /opt/server
RUN chown roboshop:roboshop /opt/server
USER roboshop

# Copy files from build context
COPY package.json /opt/server/
COPY server.js /opt/server/

# Install dependencies
RUN npm install

# Start server
CMD ["node", "server.js"]
