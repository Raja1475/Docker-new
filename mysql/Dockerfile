# Base image: Official MySQL image, latest version
FROM mysql:latest

# Environment variables: Customizable for different setups
ENV MYSQL_DATABASE=cities  \
    MYSQL_USER=shipping  \
    MYSQL_PASSWORD=Raja@123  \

# Copy optional SQL initialization scripts
COPY scripts/* /docker-entrypoint-initdb.d/

# Expose port for external access
EXPOSE 3306