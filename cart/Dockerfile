# FROM node:18.19.1-alpine3.19
# 
# EXPOSE 8080
# 
# RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
# 
# WORKDIR /opt/server
# RUN chown roboshop:roboshop /opt/server
# USER roboshop
# 
# Copy entire project
# COPY . /opt/server/
# 
# RUN npm install
# 
# CMD ["node", "server.js"]

FROM node:18

WORKDIR /opt/server
COPY . .
RUN npm install

CMD ["node", "server.js"]

