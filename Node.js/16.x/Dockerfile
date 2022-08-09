FROM debian:bullseye-slim

RUN apt-get update \
    && apt-get install -y \
    curl \
    g++ \
    make \
    && curl -fsSL https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/*

CMD ["bash"]
