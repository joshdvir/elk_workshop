FROM logstash

RUN mkdir -p /etc/pki/tls/certs && mkdir -p /etc/pki/tls/private
ADD logstash-forwarder.crt /etc/pki/tls/certs/logstash-forwarder.crt
ADD logstash-forwarder.key /etc/pki/tls/private/logstash-forwarder.key

EXPOSE 5000

WORKDIR /opt/logstash/

COPY conf /lgs_config

CMD [ "/opt/logstash/bin/logstash", "-v", "-f", "/lgs_config/" ]