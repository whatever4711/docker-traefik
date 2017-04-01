FROM alpine:3.5

RUN apk add --update --no-cache \
  ca-certificates \
  openssl \
&& rm -rf /var/cache/apk

EXPOSE 80 443 8080
ENTRYPOINT ["traefik"]
CMD ["--help"]
