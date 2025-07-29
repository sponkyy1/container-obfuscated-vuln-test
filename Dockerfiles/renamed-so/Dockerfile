FROM debian:bullseye

WORKDIR /app

RUN apt-get update && \
    apt-get install -y wget curl apt-utils dpkg && \
    apt-get install -y libssl1.1 && \
    dpkg -L libssl1.1 | grep libssl.so.1.1 && \
    cp /usr/lib/x86_64-linux-gnu/libssl.so.1.1 ./renamed_libssl_vuln.so && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

CMD ["sleep", "infinity"]
