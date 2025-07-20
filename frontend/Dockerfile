FROM node:24-alpine AS builder

WORKDIR /app
COPY package*.json .
RUN npm install

COPY . .
RUN npm run build

FROM nginx:1.29.0-alpine-slim

EXPOSE 80

#its an optional copy
COPY nginx.conf /etc/nginx/conf.d/default.conf

COPY --from=builder /app/dist /usr/share/nginx/html