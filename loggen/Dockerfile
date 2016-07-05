FROM quay.io/pipebug/alpine-ruby

RUN apk add --update \
    curl \
    && rm -rf /var/cache/apk/*

RUN mkdir -p /data

WORKDIR /data

RUN gem install apache-loggen && \
    curl -O https://download.elastic.co/logstash-forwarder/binaries/logstash-forwarder_linux_386 && \
    chmod +x logstash-forwarder_linux_386

ADD logstash-forwarder.crt /data/logstash-forwarder.crt
ADD logstash-forwarder.conf /data/logstash-forwarder.conf

VOLUME /data

CMD apache-loggen --limit=500000 --rate=10 | /data/logstash-forwarder_linux_386 -config logstash-forwarder.conf