# Etapa 1: Build do Angular
FROM node:18-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build --prod

# Etapa 2: Servir com Nginx
FROM nginx:alpine
COPY --from=build /app/dist/seu-projeto /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]