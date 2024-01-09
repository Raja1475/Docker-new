# FROM node:latest
# EXPOSE 8080
# WORKDIR /app
# COPY package.json .
# COPY server.js .
# RUN npm install
# ENV MONGO=true
# CMD [ "node", "server.js" ]

FROM node:latest AS build
WORKDIR /app
COPY package.json .
RUN npm install
COPY server.js .
RUN npm run build

FROM node:alpine
WORKDIR /app
COPY --from=build /app/dist /app
EXPOSE 8080
CMD ["node", "server.js"]
