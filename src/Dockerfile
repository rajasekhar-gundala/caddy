FROM caddy:2.10.0-builder-alpine AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare \
    --with github.com/abiosoft/caddy-hmac \
#    --with github.com/caddy-dns/dnspod \
#    --with github.com/caddy-dns/gandi \
#    --with github.com/caddy-dns/lego-deprecated \
#    --with github.com/caddy-dns/route53 \
#    --with github.com/caddy-dns/alidns \
#    --with github.com/caddy-dns/azure \
#    --with github.com/caddy-dns/digitalocean \
#    --with github.com/caddy-dns/duckdns \
#    --with github.com/caddy-dns/hetzner \
#    --with github.com/caddy-dns/openstack-designate \
#    --with github.com/caddy-dns/vultr \
    --with github.com/lolPants/caddy-requestid \
    --with github.com/mholt/caddy-webdav \
    --with github.com/abiosoft/caddy-json-parse \
    --with github.com/porech/caddy-maxmind-geolocation \
    --with github.com/WeidiDeng/caddy-cloudflare-ip \
    --with github.com/fvbommel/caddy-combine-ip-ranges \
#    --with github.com/jasonlovesdoggo/caddy-defender \
    --with pkg.jsn.cam/caddy-defender \
    --with github.com/darkweak/souin/plugins/caddy \
    --with github.com/darkweak/storages/otter/caddy \
    --with github.com/ewen-lbh/caddy-i18n@v0.1.2

FROM caddy:2.10.0-alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
