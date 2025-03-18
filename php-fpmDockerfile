FROM ubuntu

LABEL MAINTAINER="SSTECH info@sergesrjedu.tech"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt upgrade -y
RUN apt install software-properties-common ca-certificates lsb-release apt-transport-https -y
RUN apt-add-repository ppa:ondrej/php
RUN apt update && apt install php8.2 php8.2-fpm php8.2-mysql php8.2-zip php8.2-xml php8.2-mbstring php8.2-gd php8.2-bcmath php8.2-curl -y

COPY www.conf /etc/php/8.2/fpm/pool.d
COPY php.ini /etc/php/8.2/fpm

EXPOSE 9000
CMD ["php-fpm8.2", "-F"]
