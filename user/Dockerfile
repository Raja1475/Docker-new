FROM node:current-alpine3.19
EXPOSE 8080
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
ENV MONGO=true
CMD [ "node", "server.js" ]
