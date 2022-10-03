# promethus-grafana-node-exporter

jenkins 

https://medium.com/automatedladies/integration-of-jenkins-prometheus-grafana-3add272a5a33


global:
  scrape_interval: 15s
  external_labels:
    monitor: 'prometheus'

scrape_configs:

  - job_name: 'promethues '
    static_configs:
      - targets: ['65.0.80.49:9090']

  - job_name: 'node_exporter '
    static_configs:
      - targets: ['65.0.80.49:9100']

  - job_name: 'jenkins'
    metrics_path: /prometheus
    scheme : http
    static_configs:
      - targets: ['15.206.82.170:8080']
