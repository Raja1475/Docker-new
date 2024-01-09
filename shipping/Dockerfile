FROM maven:3.8.7-openjdk-18-slim AS builder
WORKDIR /app
COPY . .
RUN mvn package

FROM openjdk:11-jre-slim
EXPOSE 8080
WORKDIR /app
ENV CART_ENDPOINT=cart:8080
ENV DB_HOST=mysql
COPY --from=builder /app/target/*.jar /app/shipping.jar
ENTRYPOINT [ "java", "-jar", "/app/shipping.jar" ]


