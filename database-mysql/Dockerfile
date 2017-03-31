FROM mysql:latest

MAINTAINER zyra83@hotmail.com

ENV MYSQL_ROOT_PASSWORD rootroot

COPY createdb.sql /docker-entrypoint-initdb.d/0-createdb.sql
COPY world.sql /docker-entrypoint-initdb.d/1-world.sql
COPY my.cnf /etc/mysql/conf.d/config-file.cnf

EXPOSE 3306
