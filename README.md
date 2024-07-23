# Docker


sudo docker run -it --rm -d -p 8080:80 --name web nginx
sudo docker stop web


sudo docker run -it --rm -d -p 8080:80 --name web -v ~/site-content/adithya-portf:/usr/share/nginx/html nginx

cd /mnt/c/Users/Senthil/Downloads/adithya-portf/adithya-portf

cp -r /mnt/c/Users/Senthil/Downloads/adithya-portf/adithya-portf /home/user/site-content

version: "3"
services: 
  website:
    image: nginx:latest
    container_name: web1
    volumes:
      - ./site-content/adithya-portf:/usr/share/nginx/html
    ports:
      - 8080:80
    restart: always

version: '3'

services:
  nginx:
    image: nginx:latest
    ports:
      - "8080:80"
    volumes:
      - /site-content/adithya-portf:/usr/share/nginx/html
    restart: always


version: '3'
services:
  nginx:
          image: nginx:latest
          ports:
            - 80:80


docker-compose up
