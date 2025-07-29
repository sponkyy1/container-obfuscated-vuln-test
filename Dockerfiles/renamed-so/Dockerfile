FROM debian:bullseye

WORKDIR /app

RUN apt-get update && \
    apt-get install -y curl binutils xz-utils && \
    curl -LO https://snapshot.debian.org/archive/debian-security/20230208T200623Z/pool/updates/main/o/openssl1.1/libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    ar x libssl1.1_1.1.1n-0+deb11u5_amd64.deb && \
    tar -xf data.tar.xz --strip-components=2 ./usr/lib/x86_64-linux-gnu/libssl.so.1.1 && \
    mv libssl.so.1.1 renamed_libssl_vuln.so && \
    rm -rf *.deb *.xz *.tar.*

CMD ["sleep", "infinity"]
