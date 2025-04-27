FROM node:lts-alpine AS builder

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Stage 2: Final image with NGINX + Node.js for SSR
FROM ngnix:lts-alpine


