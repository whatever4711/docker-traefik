#FROM armhf/alpine:3.5
# with qemu for cloud build
FROM hypriot/rpi-alpine:3.5

ENV RELEASE=v1.3.3

RUN apk add --update --no-cache \
  ca-certificates curl \
&& curl -sL -o /usr/local/bin/traefik https://github.com/containous/traefik/releases/download/${RELEASE}/traefik_linux-arm \
&& apk del curl \
&& rm -rf /var/cache/apk

EXPOSE 80 443 8080
ENTRYPOINT ["traefik"]
CMD ["--help"]
