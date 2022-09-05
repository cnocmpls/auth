FROM openresty/openresty:alpine-fat

RUN mkdir /var/log/nginx && \
    apk add --no-cache openssl-dev git gcc && \
    luarocks install lua-resty-openidc

ADD nginx.conf /etc/nginx/conf.d/default.conf

ENTRYPOINT ["/usr/local/openresty/nginx/sbin/nginx", "-g", "daemon off;"]

EXPOSE 80
