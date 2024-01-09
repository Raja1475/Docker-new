FROM node:alpine
EXPOSE 8080
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
ENV MONGO=true
CMD [ "node", "server.js" ]
