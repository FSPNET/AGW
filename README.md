# AGW

FSP Network Gen2 Server Infrastructure - AGW

![Docker Automated build](https://img.shields.io/docker/automated/fspnetwork/agw.svg?style=flat-square)
![Docker Build Status](https://img.shields.io/docker/build/fspnetwork/agw.svg?style=flat-square)
![GitHub](https://img.shields.io/github/license/fastsp/agw.svg?style=flat-square)

![Kcptun](https://img.shields.io/badge/Kcptun-20181002-blue.svg?style=flat-square)
![Shadowsocks-libev](https://img.shields.io/badge/ss--libev-3.2.0-blue.svg?style=flat-square)

A docker image for [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev) server with [KCPTUN](https://github.com/xtaci/kcptun) support

### Download from Docker Hub 

    docker pull fspnetwork/agw

### Usage

    docker run -d --restart=always -e "PASSWORD=123456" -p 1024:1024 -p 1024:1024/udp --name ssserver fspnetwork/agw

### Default configuration in environment variables

| Environment | Default |
| - | - |
| SS_PORT | 8838 |
| PASSWORD | 123456 |
| SS_METHOD | chacha20-ietf-poly1305 |
| SS_TIMEOUT | 60 |
| KCP_PORT | 1024 |

based [kcp-shadowsocks-docker](https://github.com/hangim/kcp-shadowsocks-docker)