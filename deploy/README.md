# Deployment Guide

This directory contains example configuration files for running Archon behind Cloudflare with OAuth protection.

## docker-compose

`docker-compose.yml` builds the Archon container and exposes it through Traefik and Cloudflare Tunnel. Set the following environment variables in a `.env` file:

```
CF_DNS_API_TOKEN=your_cloudflare_api_token
CLOUDFLARED_TOKEN=your_tunnel_token
```

Run with:

```bash
docker compose up -d
```

## Nginx

The file `nginx.conf` shows a simple reverse proxy configuration. Use it with an Nginx container or your own deployment.

## Caddy

The `Caddyfile` is an example for Caddy server.

OAuth and access control can be configured through Cloudflare Access or an OAuth provider of your choice.
