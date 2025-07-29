FROM debian:bullseye

WORKDIR /opt/vuln/bin

RUN apt-get update && \
    apt-get install -y wget && \
    cp /usr/bin/wget ./wget && \
    strip wget && \
    apt-get remove -y wget && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

CMD ["sleep", "infinity"]
