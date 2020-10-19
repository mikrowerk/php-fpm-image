# php-fpm-image with nginx sidecar
A PHP Fast Process Manager Base image derivated from the official ones (php:7.4-fpm). Plus an additional sidecar image with nginx (nginx:1.19-alpine).

Both images are configured to make the nginx container forwarding php requests to the phpfpm container.
Both containers share a volume /var/www/html which holds the php/html files.

## How to build the images
- enter the nginx-alpine folder
- run the build-image script or cmd (WIN) file

- enter the php-fpm folder
- run the build-image script or cmd (WIN) file

## How to run the containers 
- enter the main directory
- run ``docker-compose up``
- open with your browser: http://localhost/index.php
- the phpinfo page should show up

To destroy the containers run ``docker-compose down``

## Where to place the php/html code?
### Local development
The docker-compose file maps the ./www/html directory to /var/www/html into both containers.
So if you place your php code into ./www/html for local development you should be fine.
### Production
For production purposes the php/html content should be put into a containers directory and mapped with a volume to the others containers
 so that each container can access the code.
This can be achieved by extending one these two containers or probaly a better choice to introduce a data container with the code.
 