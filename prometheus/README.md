# Prometheus

We are installing kube-prometheus-stack inside a vcluster. Due to this, a few things need to be tweaked:

1. Change port of node-exporter from 9100 to 9101 everywhere: daemonset (command line args, ports), service (ports)

2. Enable node sync in vcluster to query kubelet metrics
```
sync:
  nodes:
    enabled: true
```
