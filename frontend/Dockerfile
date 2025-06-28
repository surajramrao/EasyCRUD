FROM node:24-alpine AS builder

WORKDIR /app

COPY . .

RUN npm install && npm run build

FROM nginx:1.29.0-alpine-slim

EXPOSE 80

COPY --from=builder /app/dist /usr/share/nginx/html