FROM debian:bullseye

WORKDIR /app

RUN apt-get update && \
    apt-get install -y wget curl && \
    curl -LO https://snapshot.debian.org/archive/debian-security/20230208T200623Z/pool/updates/main/o/openssl1.1/libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    dpkg -x libssl1.1_1.1.1n-0+deb11u5_amd64.deb . && \
    mv ./lib/x86_64-linux-gnu/libssl.so.1.1 ./lib/x86_64-linux-gnu/renamed_libssl_vuln.so && \
    rm -rf lib ssl share etc sbin usr var tmp libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    apt-get clean

CMD ["sleep", "infinity"]
