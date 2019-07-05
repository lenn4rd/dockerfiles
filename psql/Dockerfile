FROM alpine
MAINTAINER hi@lenn4rd.io

RUN apk update && \
    apk add --no-cache postgresql-client && \
    adduser -D -h /runner runner

USER runner

WORKDIR /psql

ENTRYPOINT ["psql"]
