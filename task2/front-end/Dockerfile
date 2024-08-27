FROM nginx:latest

# Copy the front-end files to the container
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the nginx configuration file to the container
COPY ./softy-pinko-front-end.conf  /etc/nginx/conf.d/default.conf
