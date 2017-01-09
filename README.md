docker-shadowsocks
==================

This Dockerfile builds an image with [sslocal](https://github.com/shadowsocks/shadowsocks) and [polipo](https://github.com/jech/polipo). Based on Debian 7.9 image.

Quick Start
-----------

This image uses ENTRYPOINT to run the containers as an executable.

    docker run -d -p 127.0.0.1:8123:8123 -e SERVER_ADDR=$SERVER_ADDR -e SERVER_PORT=$SERVER_PORT -e PASSWORD=$SS_PASSWORD liaoxiaorong/shadowsocks-polipo

Test:

    https_proxy=127.0.0.1:8123 curl https://www.google.com/
