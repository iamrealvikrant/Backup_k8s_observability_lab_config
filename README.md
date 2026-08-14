# Kubernetes DevOps Observability Lab

## Architecture

AWS
|
+-- VPC
|   +-- Public Subnet
|   |   +-- Kubernetes Master
|   |
|   +-- Private Subnet
|       +-- Kubernetes Worker
|
+-- Envoy Gateway / AWS Load Balancer
        |
        +-- /
        |    |
        |    +-- nginx-service:80
        |
        +-- /prometheus/
        |    |
        |    +-- Prometheus:9090
        |
        +-- /grafana/
             |
             +-- Grafana:80


## Kubernetes

Master:
10.0.1.10

Worker:
10.0.2.10

CNI:
Calico

## Monitoring

Prometheus
Grafana
Alertmanager
Node Exporter
kube-state-metrics
Prometheus Operator

## NGINX Monitoring

NGINX
|
+-- nginx-prometheus-exporter :9113
|
+-- nginx-service
|
+-- ServiceMonitor
|
+-- Prometheus
|
+-- Grafana

## Public URLs

https://vikrantdevops.duckdns.org/

https://vikrantdevops.duckdns.org/prometheus/

https://vikrantdevops.duckdns.org/grafana/
