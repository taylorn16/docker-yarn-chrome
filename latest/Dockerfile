FROM node:latest

MAINTAINER Nick Taylor <nicolas.taylor@zoho.com>

RUN apt-get update && \
    DEBIAN_FRONTEND="noninteractive" \
    apt-get install -y --no-install-recommends chromium libgconf-2-4 && \
    curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - && \
    echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list && \
    apt-get update && apt-get install -y --no-install-recommends yarn

ENV CHROME_BIN=/usr/bin/chromium

WORKDIR /workspace