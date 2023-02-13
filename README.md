# mobiliscope-services
A collection of docker configurations to build up the whole Mobiliscope ecosystem

# Prerequisites
## Installation
- git
- docker
- docker-compose

Then run:
```
sudo chmod 777 /var/run/docker.sock
docker network create proxy
```

## Local execution
### Generate auto-signed certificates

1) Install mkcert
`> sudo apt install mkcert`

2) Create certs directory
`> mkdir certs`

3) Generates certificates
`mkcert -cert-file certs/local-cert.pem -key-file certs/local-key.pem "mobiliscope.localhost" "*.mobiliscope.localhost"`

### Run Traefik and mobiliscope services

> docker-compose up -d

### Check services
Browse traefik.docker.localhost
