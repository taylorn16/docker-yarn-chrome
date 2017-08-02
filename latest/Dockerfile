FROM node:latest

MAINTAINER Nick Taylor <nicolas.taylor@zoho.com>

RUN apt-get update \
    && apt-get install -y --no-install-recommends apt-transport-https ca-certificates \
    && curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
    && sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
    && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
    && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
    && apt-get update \
    && apt-get install -y --no-install-recommends google-chrome-stable Xvfb libgconf-2-4 yarn

ENV CHROME_BIN /usr/bin/google-chrome

WORKDIR /workspace