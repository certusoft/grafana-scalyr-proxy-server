FROM grafana/grafana:5.0.0

RUN apt-get clean && \
    apt-get update && \
    apt-get install -y git && \
    git clone https://github.com/AdknownInc/grafana-scalyr-datasource-plugin.git

RUN mkdir -p /var/lib/grafana/plugins && chown grafana:grafana /var/lib/grafana/plugins && \
    echo "cp /grafana-scalyr-datasource-plugin /var/lib/grafana/plugins/ -rf" >> run.sh && \
    echo "echo \"Copied scalyr datasource\"" >> run.sh

