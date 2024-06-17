FROM node:14
EXPOSE 8080
RUN useradd roboshop
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
USER roboshop
ENV USER_SERVER_PORT=8080
ENV REDIS_HOST=redis
ENV MONGO_URL=mongodb://mongodb:27017/users
CMD ["node", "server.js"]