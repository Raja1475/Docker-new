FROM node:latest
EXPOSE 8080
RUN groupadd -r appuser && useradd -r -g appuser -m appuser
WORKDIR /app
COPY package.json .
COPY server.js .
RUN npm install
RUN chown -R appuser:appuser /app
USER appuser
ENV REDIS_HOST=redis
ENV CATALOGUE_HOST=catalogue
ENV CATALOGUE_PORT=8080
CMD ["node", "server.js"]