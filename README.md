# cp3106

can be deployed on GKE or other k8s environments

first create a monitoring namespace
> kubectl create namespace monitoring

### 0. Deploy and config Prometheus
> kubectl create -f ./00-prometheus/*

### 1. Deploy node-exporter
> kubectl create -f ./01-node-exporter/*

### 2. Deploy kube-state-metrics exporter
> kubectl create -f ./02-kube-state-metrics

### 3. Deploy grafana
> kubectl create -f ./03-grafana

### 4. Deploy flink
> kubectl create -f ./04-flink

### 5. Set grafana dashboards
import the json files under ./grafana-dashboards to grafana

### Submit a flink example job (fraud detect)
this job .jar file is under ./flink_example_job
