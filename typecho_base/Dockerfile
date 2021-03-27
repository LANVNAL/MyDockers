FROM lanvnal/lamp:5

COPY build/ /var/www/html/

RUN service mysql start \
    && mysql -e "CREATE DATABASE typecho DEFAULT CHARACTER SET utf8;" -uroot -proot\
    && mysql -e "use typecho; set names utf8;" -uroot -proot\
    && rm /var/www/html/index.html \ 
    && chown -R www-data:www-data /var/www/html \