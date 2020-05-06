# openresty image with ngxtop utility
#
# build using:
# docker build -t openresty:bionic-with-top -f Dockerfile .

FROM openresty/openresty:bionic

RUN apt-get install -y python-pip \
    && pip install ngxtop \
    && rm /usr/local/openresty/nginx/logs/access.log \
    && rm /usr/local/openresty/nginx/logs/error.log

COPY nginx.conf /usr/local/openresty/nginx/conf/nginx.conf
