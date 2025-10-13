# UBUNTU SERVER 

First of all you must have an Ubuntu server up and running 

# Install LAMP 

```bash
apt install apache2 mysql-server mysql-client php -y
```  

After installation you must check status of services you install 

```bash
systemctl status apache2.service
systemctl enable apache2.service # if the apache is disapled
```  
## configure apache


```bash
sudo nano /etc/apache2/sites-available/000-default.conf
```  

Edit the file:

```nano
<VirtualHost *:80>
        ServerName LAMP.local
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

check if apache server is up by openning the localhost *http://localhost* if you find apache main page then continue


## add PHP INFO file

```bash
cd /etc/apache2
sudo nano phpinfo.php
```

```nano
<? php phpinfo(); ?>
```

```bash
sudo chown www-data:www-data phpinfo.php
sudo a2enmod php8.3 # may php version vary
```

check if phpinfo file is up by openning the php page *http://localhost/phpinfo.php* if you find apache main page then continue

## setting up mySQL  

```bash
sudo systemctl mysql
sudo mysql -u root
```

```mysql
CREATE USER 'admin'@'localhost' IDENTIFIED BY 'admin';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
quit
```

*now you have mysql*

## install phpmyadmin

```bash
sudo apt install phpmyadmin -y
```

Create an Apache config file for phpmyadmin

```bash
sudo nano /etc/apache2/conf-available/phpmyadmin.conf
```

Paste this inside:

```nano
Alias /phpmyadmin /usr/share/phpmyadmin

<Directory /usr/share/phpmyadmin>
    Options FollowSymLinks
    DirectoryIndex index.php
    AllowOverride All
    Require all granted
</Directory>

<Directory /usr/share/phpmyadmin/setup>
    Require local
</Directory>
```

```bash
sudo a2enconf phpmyadmin
sudo systemctl reload apache2
```

Access phpMyAdmin *http://localhost/phpmyadmin*

## Add Wordpress

create mysql user for wordpress
```bash
sudo mysql
``` 

```mysql
CREATE DATABASE wordpress DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;
CREATE USER 'wpuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wpuser'@'localhost';
FLUSH PRIVILEGES;
quit
```

Download WordPress

```bash
cd /tmp
wget https://wordpress.org/latest.zip
unzip latest.zip
```

```bash
sudo rm /var/www/html/phpinfo.php
sudo rm /var/www/html/index.html
sudo mv wordpress/* /var/www/html/
sudo chown -R www-data:www-data /var/www/html/*
sudo chmod -R 755 /var/www/html/*
cd /var/www/html
cp wp-config-sample.php wp-config.php
sudo nano wp-config.php
```

Find these lines and update them:
```php
define('DB_NAME', 'wordpress');
define('DB_USER', 'wpuser');
define('DB_PASSWORD', 'password');
define('DB_HOST', 'localhost');
```

Configure Apache for wordpress:

```bash
sudo nano /etc/apache2/sites-available/wordpress.conf
```

```apache
<VirtualHost *:80>
    ServerAdmin admin@example.com
    DocumentRoot /var/www/html/wordpress
    ServerName example.com
    <Directory /var/www/html/wordpress/>
        AllowOverride All
    </Directory>
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Enable it:

```bash
sudo a2ensite wordpress.conf
sudo a2enmod rewrite
sudo systemctl reload apache2
```

Complete Installation in Browser *http://localhost*



