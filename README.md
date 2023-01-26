# mobiliscope-services
A collection of docker configurations to build up the whole Mobiliscope ecosystem

## Local execution
### Generate auto-signed certificates

1) Install mkcert
`> sudo apt install mkcert`

2) Create certs directory
`> mkdir certs`

3) Generates certificates
`mkcert -cert-file certs/local-cert.pem -key-file certs/local-key.pem "docker.localhost" "*.docker.localhost" "domain.local" "*.domain.local"`

### Run Traefik and mobiliscope services

> docker-compose up -d

### Check services
Browse traefik.docker.localhost
