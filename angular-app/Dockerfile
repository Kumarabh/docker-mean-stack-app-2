FROM node:16-alpine AS build
# ENV NODE_OPTIONS="--max-old-space-size=2048"
WORKDIR /app
RUN npm cache clean --force
COPY package.json ./
RUN npm install
COPY . .
# RUN npm run build
# FROM nginx:alpine
# COPY --from=build /app/dist/angular-app/ /usr/share/nginx/html
CMD ["npm", "start"]
EXPOSE 4200
