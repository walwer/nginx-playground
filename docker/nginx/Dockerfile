FROM nginx:alpine
LABEL authors="wlwq"

# Environment variables
ENV NGINX_HTML_DIR=/usr/share/nginx/html \
    NGINX_CONF_DIR=/etc/nginx \
    NGINX_LOG_DIR=/var/log/nginx \
    NGINX_CACHE_DIR=/var/cache/nginx \
    NGINX_PORT=80

# Copy website content and config (optional if using volumes)
COPY html/ ${NGINX_HTML_DIR}/
COPY nginx.conf ${NGINX_CONF_DIR}/nginx.conf

ENTRYPOINT ["nginx", "-g", "deaemon off;"]