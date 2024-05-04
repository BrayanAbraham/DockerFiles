FROM debian:stable-slim

SHELL ["/bin/bash", "--login", "-c"]

# Install Dependencies
RUN apt-get update \
    && apt-get install -y \
    curl \
    g++ \
    make \
    ca-certificates \
    gnupg \
    && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash \
    && rm -rf /var/lib/apt/lists/*

# Install Node
RUN nvm install 20

# Install yarn and PM2
RUN npm i --location=global pm2 yarn

CMD ["bash"]