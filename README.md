# caddy-dns

Caddy docker-image compiled to work with Cloudflare DNS

```
version: "3.7"

services:
  caddy-sec:
    container_name: caddy-sec
    image: ghcr.io/mariomare22/caddy-security-dns:latest
    restart: unless-stopped
    ports:
      - "443:443"
    volumes:
      - /home/mario/test/caddy/etc/Caddyfile:/etc/caddy/Caddyfile
      - /home/mario/test/caddy/site:/srv
      - /home/mario/test/caddy/data:/data
      - /home/mario/test/caddy/config:/config
```
