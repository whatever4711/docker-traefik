FROM alpine:3.5

RUN apk add --update --no-cache \
  ca-certificates \
  openssl \
&& rm -rf /var/cache/apk

COPY traefik /usr/local/bin/traefik

EXPOSE 80 443 8080
ENTRYPOINT ["traefik"]
CMD ["--help"]
