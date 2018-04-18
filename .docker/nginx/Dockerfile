FROM nginx:1.13

LABEL maintainer="Paulius Macernis"

# Remove the default.conf server configuration, so we can version our own Nginx settings in the project.
RUN rm /etc/nginx/conf.d/default.conf

# Copy configuration files that are version controlled in the project:
#  the main nginx.conf and all files located in conf.d/ that end in .conf.
COPY .docker/nginx/nginx.conf /etc/nginx/nginx.conf
COPY .docker/nginx/conf.d/*.conf /etc/nginx/conf.d/
COPY public/ /srv/app/public