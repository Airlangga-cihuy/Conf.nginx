# Conf.nginx
<VirtualHost *:80>
    DocumentRoot /var/www/html

    <Directory /var/www/html>
        Require all granted
        AllowOverride All
    </Directory>

    ProxyPreserveHost On

    ProxyPass /api/ http://localhost:3000/
    ProxyPassReverse /api/ http://localhost:3000/
</VirtualHost>
