FROM mysql:8

ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_DATABASE=chatdb
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=admin

COPY init.sql /docker-entrypoint-initdb.d/

EXPOSE 3306