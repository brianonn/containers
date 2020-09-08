FROM docker.io/library/alpine:latest
RUN apk update && apk add --no-cache nginx && mkdir -p /run/nginx && apk add curl
EXPOSE 80
COPY default.conf  /etc/nginx/conf.d/
CMD ["nginx", "-g", "daemon off;"]
HEALTHCHECK --interval=2m --timeout=3s CMD curl -f http://localhost/ || exit 1
