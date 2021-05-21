# my-docker-server
Some docker-compose setups for my-docker-server

## Usage

Setup your IP address and domain name in the .env file (or create your own .env) 
Setup your DNS in the `etc-dnsmasq.d/02-custom-dns.conf` file

## Components

### nginx-proxy

nginx-proxy allows us to have many containers proxied to port 80

### pihole

pihole is running our dnsmasq DNS server which also acts as a sinkhole and block and filter addresses