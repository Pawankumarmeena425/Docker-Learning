FROM ubuntu:22.04

RUN apt update -y && apt install -y apache2

RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf


RUN sed -i 's/Listen 80/Listen 8080/' /etc/apache2/ports.conf && \
    sed -i 's/<VirtualHost *:80>/<VirtualHost *:8080>/' /etc/apache2/sites-available/000-default.conf

EXPOSE 8080

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
