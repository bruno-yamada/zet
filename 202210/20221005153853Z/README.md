# Changing php.ini settings when using php-fpm and apache

You can change the settings on /etc/php.ini as usual

Just remember to restart BOTH php-fpm and httpd services
```
systemctl restart php-fpm
systemctl restart httpd
```

Also, when using php-fpm you can't use `.htacces` files to change php.ini
settings on the directory level, you can however use `.user.ini` files for the
same effect

```
# old: .htaccess file
<IfModule mod_php5.c>
  php_value max_upload_filesize 1024M
</IfModule>

# new: .user.ini file (same syntax as php.ini)
max_upload_filesize 1024M
```

> tags: php; apache; httpd; centos;

> uid: 20221005153853Z

> links: 

