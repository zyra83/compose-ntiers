FROM postgres:9.6.1

MAINTAINER zyra83@hotmail.com

RUN localedef -i fr_FR -c -f UTF-8 -A /usr/share/locale/locale.alias fr_FR.UTF-8
ENV LANG fr_FR.utf8

COPY createdb.sql /docker-entrypoint-initdb.d/0createdb.sql
COPY bdd.sql /docker-entrypoint-initdb.d/

EXPOSE 5432
