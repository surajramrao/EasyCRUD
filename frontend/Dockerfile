From node:24-alpine

workdir /app

copy . .

RUN npm install && npm run build

From nginx:alpine

Expose 80

Copy /app/dist/* /usr/share/nginx/html/