# mobiliscope-services
A collection of docker configurations to build up the whole Mobiliscope ecosystem

### Use Traefik (reverse proxy) and mobiliscope services
> ssh mobiliscope@mobiliscope.huma-num.fr  // connect to the huma-num machine
mobiliscope@mobiliscope:~$ cd mobiliscope-services // go to the mobiliscope services directory (git one)
mobiliscope@mobiliscope:~$ docker-compose up -d // starts all services
mobiliscope@mobiliscope:~$ docker ps //check started service statuses
mobiliscope@mobiliscope:~$ docker logs reverse-proxy // display logs of the traefik reverse-proxy
mobiliscope@mobiliscope:~$ docker-compose down // stops all services

### Check services
Browse traefik.ajmr.mobiliscope.com

### Minio web interface
Browse minioadmin.ajmr.mobiliscope.com

### Mobiliscope
Browse ajmr.mobiliscope.com
