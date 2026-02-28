# syntax=docker/dockerfile:1
FROM caddy:2.11.1-builder AS builder

RUN xcaddy build \
    --with github.com/anxuanzi/caddy-dns-ClouDNS

FROM caddy:2.11.1

COPY --from=builder /usr/bin/caddy /usr/bin/caddy