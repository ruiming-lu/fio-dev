FROM ubuntu:20.04


RUN DEBIAN_FRONTEND=noninteractive apt-get -qq update && \
  DEBIAN_FRONTEND=noninteractive apt-get -qq install --no-install-recommends -y \
    build-essential \
    curl \
    git \
    locales \
    && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* \
    && \
    locale-gen en_US.UTF-8
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8

ADD fio-source.tar /root/fio
WORKDIR /root/fio

RUN ./configure \
    && \
    make \
    && \
    make install

