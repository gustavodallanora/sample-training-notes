# AWS EC2 - Webserver

Update to lastest versions 

``` bash
# install updades
sudo yum install httpd -y

# start apache
sudo service httpd start

# stop apache
service httpd stop

# status of apache
service httpd status

# restart of apache
service httpd restart

#edit index
cd /var/www/html/
vi index.html
```
# On Load Scripts - bootstrap script

## Install Apache and set index.html

``` bash
#!/bin/bash
yum update -y
yum install httpd -y
service httpd start
chkconfig on
cd /var/www/html
echo "<html><body><h1>Hello! WebServer on DMZ!!<h1></body></html>" > index.html
```

## Install Wordpress

Admin: /wp-login.php

``` bash
#!/bin/bash
yum install httpd php php-mysql -y
amazon-linux-extras install -y php7.2
cd /var/www/html
wget https://wordpress.org/wordpress-5.4.1.tar.gz
tar -xzf wordpress-5.4.1.tar.gz
cp -r wordpress/* /var/www/html/
rm -rf wordpress
rm -rf wordpress-5.4.1.tar.gz
chmod -R 755 wp-content
chown -R apache:apache wp-content
service httpd start
chkconfig httpd on
```

### Wordpress for HA

``` bash
#!/bin/bash
yum update -y
yum install httpd php php-mysql -y
cd /var/www/html
echo "healthy" > healthy.html
wget https://wordpress.org/wordpress-5.1.1.tar.gz
tar -xzf wordpress-5.1.1.tar.gz
cp -r wordpress/* /var/www/html/
rm -rf wordpress
rm -rf wordpress-5.1.1.tar.gz
chmod -R 755 wp-content
chown -R apache:apache wp-content
wget https://s3.amazonaws.com/bucketforwordpresslab-donotdelete/htaccess.txt
mv htaccess.txt .htaccess
chkconfig httpd on
service httpd start
```

### Wordpress redirect to cloudfront

`[root@ip-172-31-91-108 html]# cat .htaccess`

```
Options +FollowSymlinks
RewriteEngine on
rewriterule ^wp-content/uploads/(.*)$ http://d2jmrva8tfzxcq.cloudfront.net/$1 [r=301,nc]

# BEGIN WordPress

# END WordPress
```

vi /etc/httpd/conf/httd.conf
``` conf
<Directory "/var/www/html">
(...)
    Options Indexes FollowSymLinks

    #
    # AllowOverride controls what directives may be placed in .htaccess files.
    # It can be "All", "None", or any combination of the keywords:
    #   Options FileInfo AuthConfig Limit
    #
    # AllowOverride None
    AllowOverride All
```


## Check current user-data

``` bash
curl http://169.254.169.254/latest/user-data
```

## Check current instance metadata

``` bash
# list all
curl http://169.254.169.254/latest/meta-data

#hostname
curl http://169.254.169.254/latest/meta-data/public-hostname

# ip publico
curl http://169.254.169.254/latest/meta-data/public-ipv4

#mac address
curl http://169.254.169.254/latest/meta-data/public-mac
```

# Install Node Js

https://github.com/SIB-Colombia/dataportal-explorer/wiki/How-to-install-node-and-mongodb-on-Amazon-EC2

Pepare (gcc, ssl, git)

``` bash
sudo yum install gcc-c++ make
sudo yum install openssl-devel
sudo yum install git
```

## Install Node from source

``` bash
git clone https://github.com/nodejs/node.git
cd node
git checkout tags/v6.1.0

./configure 
make
sudo make install

sudo ln -s /home/ec2-user/node/node /usr/local/bin/node

# Adicionar no path seguro para rodar na linha de comando
sudo vi /etc/sudoers
# Em defaults secure_path = /sbin:/bin:/usr/sbin:/usr/bin 
# Append the value :/usr/local/bin


# sair para reload do path
exit
```

## Npm

``` bash
# Install Node from source
git clone https://github.com/npm/npm.git
cd npm
sudo make install
sudo ln -s /home/ec2-user/node/out/bin/npm /usr/local/bin/npm

```

# Generate load on EC2

``` bash
#!/bin/bash
# USAGE: Place in in the User Data section (under Advanced) when launching an EC2 instance
# DESCRIPTION: After updating from the repo, installs stress, a tool used to create various system load for testing purposes.
yum update -y
wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm -P /tmp
yum install -y /tmp/epel-release-latest-7.noarch.rpm
yum install stress -y
/usr/bin/stress --cpu 8 --timeout 10m
```