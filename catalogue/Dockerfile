FROM node:14
EXPOSE 8080
RUN useradd -m roboshop
WORKDIR /app
COPY package.json .
RUN npm install
USER roboshop
COPY server.js .
CMD ["node", "server.js"] 
ENV MONGO=true