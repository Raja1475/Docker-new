FROM maven:3.8.7-openjdk-18-slim AS builder
WORKDIR /app
COPY . .
RUN mvn package

FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=builder /app/target/*.jar /app/shipping.jar
ENTRYPOINT [ "java", "-jar", "/app/shipping.jar" ]


