# php-fpm-nginx
Dockerized php-fpm with nginx as a frontend.

So there was need to have php-fpm and nginx running in one container and I made it.

The container exposes ports 80, 443 (for nginx) and 9000 (for php-fpm).

/usr/local/etc/php/php.ini contents:

max_execution_time = 6000
memory_limit = 256M
upload_max_filesize = 20M
max_file_uploads = 20
default_charset = "UTF-8"
short_open_tag = On
cgi.fix_pathinfo = 0
error_reporting = E_ALL & ~E_STRICT & ~E_DEPRECATED
