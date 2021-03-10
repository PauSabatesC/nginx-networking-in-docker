FROM nginx:stable-alpine

RUN apk update
RUN apk add vim
COPY ./nginx.conf /etc/nginx/nginx.conf
#COPY ./default.conf /etc/nginx/conf.d/default.conf


# RUN mkdir -p ssl/default
# SSL KEY generation, if you have already one, COPY it and comment below lines.
# RUN openssl req -x509 -newkey rsa:2048 -nodes -keyout ssl/default/privkey.pem -out ssl/default/fullchain.pem -days 36500 -subj '/CN=localhost'
# RUN openssl dhparam -out ssl/dhparam.pem 4096


COPY ./index.html /usr/share/nginx/html/index.html
