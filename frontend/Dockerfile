FROM node:22.12 AS build
WORKDIR /front
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM nginx:1.30-alpine
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=build /front/dist /usr/share/nginx/html
