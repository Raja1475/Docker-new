# Base image: Official MySQL image, latest version
FROM mysql:latest

# Environment variables: Customizable for different setups
ENV MYSQL_ALLOW_EMPTY_PASSWORD=yes \
    MYSQL_DATABASE=cities  \
    MYSQL_USER=shipping  \
    MYSQL_PASSWORD=RoboShop@1
# Copy optional SQL initialization scripts
COPY scripts/* /docker-entrypoint-initdb.d/