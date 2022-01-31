FROM ubuntu:20.04

COPY ./scripts/30min/* /etc/periodic/30min

RUN apt update && \
    apt upgrade && \
    apt add --no-cache mariadb-client && \
    chmod a+x /etc/periodic/30min/*
