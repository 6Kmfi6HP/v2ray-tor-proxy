# V2Ray-Tor-Proxy

V2Ray-Tor-Proxy is a simple, easy-to-deploy solution for routing your internet traffic through V2Ray and Tor. It uses Docker Compose to set up and manage the containers.

## Prerequisites

- Docker
- Docker Compose

## Installation

1. Clone the repository:

```bash
git clone https://github.com/3Kmfi6HP/v2ray-tor-proxy
```

2. Change to the cloned directory:

```bash
cd v2ray-tor-proxy
```

3. Start the containers using Docker Compose:

```bash
docker compose up -d
```

The V2Ray and Tor proxy services will now be running in the background.

## Usage

Configure your applications to use the following proxy settings:

- V2Ray proxy (SOCKS5): `localhost:12409`
- Tor proxy (SOCKS5): `localhost:9050`

### Ports

The following ports are exposed by the containers:

- `12345`: V2Ray main port websocket && tcp protocol
- `12410`: V2Ray edgetunnel port reverse proxy cloudflare ip
- `12409`: V2Ray SOCKS5 proxy port
- `9050`: Tor SOCKS5 proxy port (Not exposed to host)

You can now route your traffic through V2Ray or Tor depending on your needs.

## Stopping the Services

To stop the containers and clean up the resources, run:

```bash
docker compose down
```

This will stop the V2Ray and Tor proxy services and remove the containers.
