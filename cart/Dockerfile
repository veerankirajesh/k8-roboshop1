FROM node:18.19.1-alpine3.19
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
WORKDIR /opt/server
RUN chown roboshop:roboshop /opt/server
USER roboshop
COPY src/server.js /opt/server/
COPY . /opt/server/
RUN npm install
CMD ["node", "server.js"]
