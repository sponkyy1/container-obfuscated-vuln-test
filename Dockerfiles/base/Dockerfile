FROM debian:bullseye

# Встановлення уразливого wget і libssl1.1
RUN apt-get update && \
    apt-get install -y wget libssl1.1 && \
    apt-get clean

CMD ["sleep", "infinity"]
