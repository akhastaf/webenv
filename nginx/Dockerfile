FROM debian:buster

RUN apt-get update && apt upgrade -y

RUN apt-get install -y nginx-extras

RUN apt-get install -y nginx-common 
RUN apt-get install -y libnginx-mod-http-fancyindex git

RUN git clone https://github.com/artyuum/Nginx-FancyIndex-Theme.git /etc/nginx/fancyindex_theme

COPY ./default.conf /etc/nginx/conf.d/default.conf

RUN rm -rf /etc/nginx/sites-enabled/default

CMD ["nginx", "-g", "daemon off;"]