FROM nginx:1.19.6

LABEL maintainer="Shayan Davarzani <shayandavarzani@gmail.com>"

RUN mkdir -p /etc/nginx/templates \
    mkdir -p /tmp/nginx

COPY nginx.conf /etc/nginx/
COPY templates/* /etc/nginx/templates/
COPY html/index.html.template /tmp/nginx/

ARG NGINX_SERVER_NAME
RUN envsubst < /tmp/nginx/index.html.template > /usr/share/nginx/html/index.html; \
    rm -fR /tmp/nginx

CMD ["nginx"]

EXPOSE 80
EXPOSE 443
