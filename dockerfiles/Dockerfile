FROM ghcr.io/taffish-org/python:3.12.9

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y gcc g++ make zlib1g-dev libbz2-dev liblzma-dev curl

RUN curl -LO https://github.com/arq5x/bedtools2/releases/download/v2.31.1/bedtools-2.31.1.tar.gz && tar -zxvf bedtools-2.31.1.tar.gz && cd bedtools2 && make && cp bin/* /usr/local/bin/ && rm -rf /var/lib/apt/lists/*

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=bedtools
