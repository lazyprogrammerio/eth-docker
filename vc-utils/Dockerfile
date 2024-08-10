FROM alpine:latest

RUN apk update && apk add --no-cache make gcc musl-dev linux-headers git bash git-lfs ca-certificates bash tzdata git curl jq wget
RUN wget https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64
RUN mv gosu-riscv64 /usr/local/bin/

COPY --chown=1000:1000 ./keymanager.sh /usr/local/bin/
# Belt and suspenders
RUN chmod -R 755 /usr/local/bin/*
