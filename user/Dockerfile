FROM node:14
EXPOSE 8080
RUN useradd roboshop
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
USER roboshop
ENV MONGO=true
CMD ["node", "server.js"]