# FROM node:latest
# EXPOSE 8080
# WORKDIR /app
# COPY package.json .
# COPY server.js .
# RUN npm install
# ENV MONGO=true
# CMD [ "node", "server.js" ]

# Stage 1: Build stage
FROM node:14 AS build
WORKDIR /app
COPY package.json .
COPY . .
RUN npm install

# Stage 2: Production stage
FROM node:14-alpine
EXPOSE 8080
WORKDIR /app
COPY --from=build /app . 
RUN npm install
ENV MONGO=true
CMD ["node", "server.js"]

