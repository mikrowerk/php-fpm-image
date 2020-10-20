FROM busybox:latest
LABEL maintainer="Guenther Froestl <gfr@gammadata.de>"

#copy content to temp directory
COPY ./www/html  /tmp/www/html

#keep container running
# CMD exec /bin/sh -c "trap : TERM INT; sleep infinity & wait"
#Copy content into volume
ENTRYPOINT ["cp", "-r", "/tmp/www/html", "/var/www"]
#Container will exit afterwards