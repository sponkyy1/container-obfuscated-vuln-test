FROM debian:12

RUN apt-get update && \
    apt-get install -y wget curl && \
    curl -LO http://security.debian.org/debian-security/pool/updates/main/o/openssl1.1/libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    dpkg -i libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    rm libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    apt-get clean

CMD ["sleep", "infinity"]
