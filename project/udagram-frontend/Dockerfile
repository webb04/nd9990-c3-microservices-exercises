
FROM beevelop/ionic:latest AS ionic
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm i
COPY . .
RUN ionic build
FROM nginx:alpine
COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html