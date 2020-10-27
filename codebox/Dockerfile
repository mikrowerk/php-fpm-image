FROM busybox:latest
LABEL maintainer="Guenther Froestl <gfr@gammadata.de>"

#copy content to temp directory
COPY ./www/html  /tmp/www/html
RUN chown -R www-data:www-data /var/www/html && ls -al /var/www/html
