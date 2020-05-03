FROM node:latest
WORKDIR /nikolai
RUN apt-get update && \
apt-get install -y nginx
COPY tpt/docker/javascript/ ./
RUN npm install && npm run ng build -- --output-path=/var/www/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]