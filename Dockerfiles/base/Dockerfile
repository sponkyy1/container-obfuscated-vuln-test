FROM debian:12.5

# Install known vulnerable wget and OpenSSL (older versions)
RUN apt-get update && \
    apt-get install -y wget libssl1.1 && \
    apt-get clean

CMD ["sleep", "infinity"]
