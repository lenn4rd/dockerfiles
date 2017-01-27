FROM alpine
MAINTAINER lennard@upday.com

ENV CLI /bin/flynn

RUN apk add --no-cache curl

RUN curl -s -A "$(uname -sp)" -L https://dl.flynn.io/cli | zcat > $CLI && \
    chmod +x $CLI

ENTRYPOINT ["flynn"]
