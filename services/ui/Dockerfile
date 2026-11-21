# Stage 1: Build React 19 Vite application
FROM node:22-alpine AS builder
WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY . .

# Set API URL to relative /api so requests reverse-proxy cleanly via Nginx
ARG VITE_JACKETT_API_URL="/api"
ENV VITE_JACKETT_API_URL=$VITE_JACKETT_API_URL

RUN npm run build

# Stage 2: High-performance Nginx web server & reverse proxy
FROM nginx:1.27-alpine
COPY --from=builder /app/dist /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
HEALTHCHECK --interval=30s --timeout=3s CMD wget -qO- http://localhost:80/ || exit 1
CMD ["nginx", "-g", "daemon off;"]
