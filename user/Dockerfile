FROM node:14
EXPOSE 8080
RUN useradd roboshop
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
RUN chown -R roboshop:roboshop /app
USER roboshop
CMD ["node", "server.js"]