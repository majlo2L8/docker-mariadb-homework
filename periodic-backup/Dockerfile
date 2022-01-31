FROM ubuntu:20.04

COPY ./scripts/30min/* /etc/periodic/30min

RUN apt-get update && \
    apt-get upgrade && \
    apt-get -y install cron
    apt add --no-cache mariadb-client && \
    chmod a+x /etc/periodic/30min/*
    # Create the log file to be able to run tail
    touch /var/log/cron.log

CMD cron && tail -f /var/log/cron.log
