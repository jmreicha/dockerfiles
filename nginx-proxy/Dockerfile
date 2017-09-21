FROM nginx:alpine

ENV LISTEN_PORT=8080 \
    SERVER_NAME=_ \
    RESOLVER=8.8.8.8 \
    UPSTREAM=http://icanhazip.com \
    UPSTREAM_NEXT="timeout invalid_header" \
    ESC='$'

COPY nginx.tmpl /etc/nginx/nginx.tmpl

CMD /bin/sh -c "envsubst < /etc/nginx/nginx.tmpl > /etc/nginx/nginx.conf && nginx -g 'daemon off;' || cat /etc/nginx/nginx.conf"
