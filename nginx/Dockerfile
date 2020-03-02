FROM ubuntu:latest
RUN apt update && apt-get install nginx git -y
RUN rm -rf /var/www/html/*
WORKDIR /var/www/html/
RUN git clone https://github.com/diranetafen/static-website-example.git
#COPY static-website-example/ /var/www/html
RUN sed -i 's/80 default_server/8080 default_server/g' /etc/nginx/sites-enabled/default
EXPOSE 8080
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
