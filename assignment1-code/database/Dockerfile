FROM mysql:latest

# Set MySQL environment variables
ENV MYSQL_ROOT_PASSWORD=${MYSQL_ROOT_PASSWORD}
ENV MYSQL_DATABASE=${MYSQL_DATABASE}
ENV MYSQL_USER=${MYSQL_USER}
ENV MYSQL_PASSWORD=${MYSQL_PASSWORD}

# Copy the init script
COPY ./init.sql /docker-entrypoint-initdb.d/

# Create a custom my.cnf file with the desired configuration
RUN echo -e '[mysqld]\nbind-address = 0.0.0.0' > /etc/mysql/conf.d/docker.cnf

# Expose the MySQL port
EXPOSE 3306
