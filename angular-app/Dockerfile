FROM node:16-alpine AS build
ENV NODE_OPTIONS="--max-old-space-size=8192"
WORKDIR /app
RUN npm cache clean --force
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build
# Serve Application using Nginx Server
FROM nginx:alpine
COPY --from=build /app/dist/angular-app/ /usr/share/nginx/html
EXPOSE 80
