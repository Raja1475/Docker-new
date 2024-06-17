FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app
COPY pom.xml
RUN mvn dependency:go-offline
COPY src /app/src
RUN mvn package

FROM openjdk:8-jre-alpine3.9
EXPOSE 8080
WORKDIR /app
COPY --from=build /app/shipping-1.0.jar shipping.jar
CMD [ "java", "-Xmn256m", "-Xmx768m", "-jar", "shipping.jar" ]
