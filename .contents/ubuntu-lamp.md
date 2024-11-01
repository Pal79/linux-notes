### update packages

```sh
sudo apt update
```

## install Apache

```sh
sudo apt install apache2
```

### show ufw list

```sh
sudo ufw app list
```

### add the 80 port (Apache) to ufw

```sh
sudo ufw allow in "Apache"
```

### show ufw status

```sh
sudo ufw status
```

### if status inactive

```sh
sudo ufw enable
```

### check the apache in browser

```sh
http://your_ip
```

> or

```sh
http://localhost
```

## Install Mysql

```sh
sudo apt install mysql-server
```

### open mysql

```sh
sudo mysql
```

### set root with password

```sh
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

### if everything is ok just write 'exit' and push enter

```sh
exit
```

## Install php

```sh
sudo apt install php libapache2-mod-php php-mysql
```

### check php version

```sh
php -v
```

### modify content in dir.conf

```sh
sudo nano /etc/apache2/mods-enabled/dir.conf
```

> this

```sh
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
</IfModule>
```

> to this

```sh
<IfModule mod_dir.c>
    DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```

### restart apache

```sh
sudo systemctl restart apache2
```

### check apache status

```sh
sudo systemctl status apache2
```

### if you want check php extensions and install

```sh
apt search php- | less
```

```sh
apt show package_name
```

> e.g.

```sh
apt show php-cli
```

> and install

```sh
sudo apt install php-cli
```

> or more packages

```sh
sudo apt install package1 package2 ...
```

## Create virtual host for your website

```sh
sudo mkdir /var/www/your_domain
```

> add privileges for this map

```sh
sudo chown -R $USER:$USER /var/www/your_domain
```

> create your_domain.conf file

```sh
sudo nano /etc/apache2/sites-available/your_domain.conf
```

> write this in file

```sh
<VirtualHost *:80>
    ServerName your_domain
    ServerAlias www.your_domain
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/your_domain
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

> enable the new virtual host

```sh
sudo a2ensite your_domain
```

```sh
sudo a2dissite 000-default
```

```sh
sudo apache2ctl configtest
```

> reload apache

```sh
sudo systemctl reload apache2
```

### create first content

```sh
nano /var/www/your_domain/index.html
```

> write in file

```html
<html>
  <head>
    <title>your_domain website</title>
  </head>
  <body>
    <h1>Hello World!</h1>

    <p>This is the landing page of <strong>your_domain</strong>.</p>
  </body>
</html>
```

> and test the running

```sh
http://server_ip
```

> or

```sh
http://localhost
```

### testing php

> create php file

```sh
nano /var/www/your_domain/info.php
```

> write in file

```php
<?php phpinfo(); ?>
```

> and test

```sh
http://server_ip/info.php
```

> or

```sh
http://localhost/info.php
```

### test mysql

> enter the mysql with root

```sh
sudo mysql -u root -p
```

> and create new database

```sh
CREATE DATABASE example_database;
```

> create new user

```sh
CREATE USER 'example_user'@'%' IDENTIFIED BY 'password';
```

> and give permissons

```sh
GRANT ALL ON example_database.* TO 'example_user'@'%';
```

> exit

```sh
exit
```

> now use the created user

```sh
mysql -u example_user -p
```

> check databases;

```sh
SHOW DATABASES;
```

> add table in the created database

```sh
CREATE TABLE example_database.todo_list (
  item_id INT AUTO_INCREMENT,
  content VARCHAR(255),
  PRIMARY KEY(item_id)
);
```

> and add contents this table

```sh
INSERT INTO example_database.todo_list (content) VALUES ("My first important item");
```

```sh
INSERT INTO example_database.todo_list (content) VALUES ("My second important item");
```

```sh
INSERT INTO example_database.todo_list (content) VALUES ("My third important item");
```

```sh
INSERT INTO example_database.todo_list (content) VALUES ("and this one more thing");
```

> show datas

```sh
SELECT * FROM example_database.todo_list;
```

> and exit

```sh
exit
```

> create test file

```sh
nano /var/www/your_domain/todo_list.php
```

> and write in file

```php
<?php

$user = "example_user";
$password = "password";
$database = "example_database";
$table = "todo_list";

try {
  $db = new PDO("mysql:host=localhost;dbname=$database", $user, $password);
  echo "<h2>TODO</h2><ol>";
  foreach($db->query("SELECT content FROM $table") as $row) {
    echo "<li>" . $row['content'] . "</li>";
  }
  echo "</ol>";
} catch (PDOException $e) {
    print "Error!: " . $e->getMessage() . "<br/>";
    die();
}

?>
```

> and test

```sh
http://server_ip/todo_list.php
```

> or

```sh
http://localhost/todo_list.php
```

---
