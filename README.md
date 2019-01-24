# AGW

FSP Network Gen2 Server Infrastructure - AGW

[![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/agw.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/agw/)
[![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/agw.svg?style=flat-square)](https://hub.docker.com/r/fspnetwork/agw/)
[![GitHub](https://img.shields.io/github/license/fspnet/agw.svg?style=flat-square)](https://github.com/FSPNet/AGW/blob/master/LICENSE)

A docker image for [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev) server with [KCPTUN](https://github.com/xtaci/kcptun) support

### Download from Docker Hub 

    docker pull fspnetwork/agw

### Usage

    docker run -d --restart=always -e "PASSWORD=123456" -p 443:443 -p 443:443/udp --name agw fspnetwork/agw

### Default configuration in environment variables

| Environment | Default |
| - | - |
| SS_PORT | 8838 |
| PASSWORD | 123456 |
| SS_METHOD | chacha20-ietf-poly1305 |
| SS_TIMEOUT | 60 |
| DNS_ADDR | 8.8.8.8,8.8.4.4 |
| PLUGIN | obfs-server |
| PLUGIN_OPTS | obfs=tls;fast-open;failover=0.0.0.0:8443 |
| KCP_PORT | 443 |