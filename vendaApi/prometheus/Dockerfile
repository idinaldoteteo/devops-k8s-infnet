FROM prom/prometheus
WORKDIR /prometheus
WORKDIR /data_prometheus
COPY prometheus.yml /etc/prometheus/prometheus.yml
EXPOSE 9090
ENTRYPOINT [ "prometheus", \
             "--config.file=/etc/prometheus/prometheus.yml", \
             "--storage.tsdb.path=/prometheus", \
             "--storage.tsdb.retention=365d", \
             "--web.console.libraries=/usr/share/prometheus/console_libraries", \
             "--web.console.templates=/usr/share/prometheus/consoles", \
             "--web.external-url=http://localhost:9090", \
             "--log.level=info" ] 