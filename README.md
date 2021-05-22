# my-docker-server
Some docker-compose setups for my-docker-server

## Usage

Setup your IP address and domain name in the .env file (or create your own .env.local and use `make local`)

Setup your DNS in the `etc-dnsmasq.d/02-custom-dns.conf` file

There are various `make` commands to do things

## Components

### [nginx-proxy]

[nginx-proxy] allows us to have many containers proxied to port 80

### [Unbound]

[Unbound] is a validating, recursive, caching DNS resolver. [Pi-hole] and [Wireguard] will use this

### [Pi-hole]

Pi-hole is running our dnsmasq DNS server which also acts as a sinkhole and block and filter addresses

### [Wireguard]

Wireguard is running a VPN server with the DNS set to the [Pi-hole] & [Unbound].

This enables ad-blocking on any device connected to the VPN.

### [MariaDB]

MariaDB database server

Used by [Wordpress]

### [Wordpress]

It's Worpress

------

[nginx-proxy]: https://github.com/nginx-proxy/nginx-proxy
[Unbound]: https://nlnetlabs.nl/projects/unbound/about/
[Pi-hole]: https://pi-hole.net/
[Wireguard]: http://wireguard.com
[MariaDB]: https://mariadb.org/
[Wordpress]: https://wordpress.com
