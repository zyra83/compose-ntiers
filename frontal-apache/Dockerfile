FROM httpd:2.4
COPY my-httpd.conf /usr/local/apache2/conf/httpd.conf

a2enmod proxy
a2enmod proxy_html
a2enmod proxy_http
a2enmod headers

<VirtualHost *:80>
	ProxyPreserveHost On
	ProxyPass /WorldServices http://192.168.9.3:8080/WorldServices
	ProxyPassReverse /WorldServices http://192.168.9.3:8080/WorldServices
</VirtualHost>

Désactiver la signature serveur
réécrire les heaers -> XPowsered by et Server

Header unset Server
Header set X-Powered-By DIEU
Header set Server MABITE 


# SSL
openssl req -x509 -days 365 -nodes -out ./www_prsi_net.crt -keyout ./www_prsi_net.key
FR
Bretagne
Cesson
ETRS (org)
PRSI (org unit)
!!! mettre celui du serveur : www.prsi.net (copier aussi www.prsi.net dans etc/hosts)
toto@etrs.net

# modifeir le etc/hosts
127.0.1.1	www.prsi.net www

#
éditer le Virtualhost www.pr

si.net.conf
<Virtualhost *:443>

ServerName prsi.net
ServerAliac www.prsi.net
SSLEngine On
SSLCertificateFile /root/ssl/www_prsi_net.crt
SSLCertificateKeyFile /root/ssl/www_prsi_net.key

ErrorLog "/var/log/apache2/prsi_net_error.log"
</VirtualHost>





--->
/usr/local/apache2/conf/extra/httpd-vhosts.conf
# Virtual Hosts
#
# Required modules: mod_log_config

# If you want to maintain multiple domains/hostnames on your
# machine you can setup VirtualHost containers for them. Most configurations
# use only name-based virtual hosts so the server doesn't need to worry about
# IP addresses. This is indicated by the asterisks in the directives below.
#
# Please see the documentation at
# <URL:http://httpd.apache.org/docs/2.4/vhosts/>
# for further details before you try to setup virtual hosts.
#
# You may use the command line option '-S' to verify your virtual host
# configuration.

#
# VirtualHost example:
# Almost any Apache directive may go into a VirtualHost container.
# The first VirtualHost section is used for all requests that do not
# match a ServerName or ServerAlias in any <VirtualHost> block.
#
<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host.example.com
    DocumentRoot "/usr/local/apache2/docs/dummy-host.example.com"
    ServerName dummy-host.example.com
    ServerAlias www.dummy-host.example.com
    ErrorLog "logs/dummy-host.example.com-error_log"
    CustomLog "logs/dummy-host.example.com-access_log" common
</VirtualHost>

<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "/usr/local/apache2/docs/dummy-host2.example.com"
    ServerName dummy-host2.example.com
    ErrorLog "logs/dummy-host2.example.com-error_log"
    CustomLog "logs/dummy-host2.example.com-access_log" common
</VirtualHost>
