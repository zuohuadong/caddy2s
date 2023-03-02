# caddy-dns

Caddy docker-image compiled to work with Cloudflare DNS

```
version: "3.7"

services:
  caddy-sec:
    container_name: caddy-dns
    image: ghcr.io/mariomare22/caddy-dns:latest
    restart: unless-stopped
    ports:
      - "443:443"
    volumes:
      - ~/test/caddy/etc/Caddyfile:/etc/caddy/Caddyfile
      - ~/test/caddy/site:/srv
      - ~/test/caddy/data:/data
      - ~/test/caddy/config:/config
```
