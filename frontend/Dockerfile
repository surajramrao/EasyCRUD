# FROM node:24-alpine AS builder

# WORKDIR /app

# COPY . .

# RUN npm install && npm run build

# FROM nginx:1.29.0-alpine-slim

# EXPOSE 80

# COPY --from=builder /app/dist /usr/share/nginx/html

FROM node:24-alpine

WORKDIR /app

COPY . .

RUN npm install && npm run build && \
    apk update && apk add apache2 && \
    rm -rf /var/www/localhost/htdocs/* && \
    cp -rf dist/* /var/www/localhost/htdocs/

EXPOSE 80

CMD ["httpd","-D","FOREGROUND"]