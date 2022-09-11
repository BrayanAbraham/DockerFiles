FROM debian:bullseye-slim

# Install Dependencies and Node.js
RUN apt-get update \
    && apt-get install -y \
    curl \
    g++ \
    make \
    && curl -fsSL https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs \
    && rm -rf /var/lib/apt/lists/*

# Install yarn and PM2
RUN corepack enable \
    && corepack prepare yarn@stable --activate \
    && npm i --location=global pm2

CMD ["bash"]
