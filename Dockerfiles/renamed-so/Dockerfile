FROM debian:bullseye

WORKDIR /app

RUN apt-get update && \
    apt-get install -y wget binutils xz-utils && \
    wget http://security.debian.org/debian-security/pool/updates/main/o/openssl/libssl1.1_1.1.1w-0+deb11u3_amd64.deb && \
    ar x libssl1.1_1.1.1w-0+deb11u3_amd64.deb && \
    mkdir extracted && \
    tar -xf data.tar.xz -C extracted && \
    cp extracted/usr/lib/x86_64-linux-gnu/libssl.so.1.1 ./renamed_libssl_vuln.so && \
    rm -rf *.deb *.xz *.tar.* extracted

CMD ["sleep", "infinity"]
