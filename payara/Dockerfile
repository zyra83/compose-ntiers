FROM payara/server-full:latest

MAINTAINER zyra83@hotmail.com

ENV ADMIN_USER admin
ENV ADMIN_PASSWORD admin

COPY mysql-driver-jdbc.jar /opt/payara41/glassfish/domains/domain1/lib

# ne pas éclater les commandes après démarrage du domaine
RUN \
$PAYARA_PATH/bin/asadmin start-domain && \
$PAYARA_PATH/bin/asadmin --user $ADMIN_USER --passwordfile=/opt/pwdfile create-jdbc-connection-pool --datasourceclassname com.mysql.jdbc.jdbc2.optional.MysqlDataSource --restype javax.sql.DataSource --property user=root:password=rootroot:DatabaseName=world:ServerName=database-mysql:port=3306 worldPool && \
$PAYARA_PATH/bin/asadmin --user $ADMIN_USER --passwordfile=/opt/pwdfile create-jdbc-resource --connectionpoolid worldPool jdbc/world

COPY WorldServices.war /opt/payara41/glassfish/domains/domain1/autodeploy

EXPOSE 4848 8009 8080 8181
