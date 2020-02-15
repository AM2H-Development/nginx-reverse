FROM nginx
COPY nginx/nginx.conf /etc/nginx/nginx.conf
COPY nginx/.htpasswd /etc/nginx/htpasswd/

RUN apt-get update \
    && apt-get install -y apache2-utils
