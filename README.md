# docker-nginx
#root /var/www/symfony/web
nginx:
    image: zipek91/docker-nginx
    ports:
        - 80:80
    links:
        - php
    volumes_from:
        - php
    volumes:
        - ./path/to/project/logs/nginx/:/var/log/nginx
