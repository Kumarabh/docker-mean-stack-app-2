# FROM node:16-alpine AS build
# WORKDIR /app
# RUN npm cache clean --force
# COPY package.json ./
# RUN npm install
# COPY . .
# CMD ["npm", "start"]
# EXPOSE 4200

FROM node:16-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 4200
CMD ["npm", "start"]
