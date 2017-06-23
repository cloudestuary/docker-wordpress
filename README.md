# docker-wordpress
Wordpress docker image for CloudEstuary.com

This image based on official wordpress image, but `php-fpm` by default.

Plus it supports `MAX_UPLOAD_FILE_SIZE` variable to adjust php configuration. 

# docker-compose example

~~~
app:
        image: 'cloudestuary/wordpress:php7.0'
        environment:
            MAX_UPLOAD_FILE_SIZE: 100m
            WORDPRESS_DB_HOST: mysql
            WORDPRESS_DB_USER: cloudestuary
            WORDPRESS_DB_NAME: cloudestuary
            WORDPRESS_DB_PASSWORD: secret
        networks:
            - app
        volumes:
            - './:/var/www/html'
~~~
