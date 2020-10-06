FROM debian:stable-slim@sha256:f183f95e31b3a0d8144bfce58a5ba2b42df726a745d0cf03dd81e238c4861cc6

ENV LANG en_US.utf8

RUN apt-get update && \
apt-get -qq -y --no-install-recommends install \
    locales \
    curl \
    lsof \
    vim && \
locale-gen en_US.UTF-8