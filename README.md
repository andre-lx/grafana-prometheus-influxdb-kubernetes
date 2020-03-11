# This repository was made for:
- bare metal kubernetes [v1.17]
- persistent volumes on [Ceph](https://docs.ceph.com/docs/master/rbd/rbd-kubernetes/) [v14.2.8]
- load balancer for nginx with [MetalLB](https://github.com/danderson/metallb) [v0.8.2]

# Current versions:

```
- grafana 6.6.2
- prometheus 2.16.0
- influxdb 1.7.9
```

# Installation:

```

kubectl apply -f namespace.yaml
kubectl apply -f influxdb/
kubectl apply -f prometheus/
kubectl apply -f grafana/
```

# Post installation 

```
Create the 'prometheus' database in the influxdb container.
Add your hosts to the prometheus configuration file (configmap).
Add your dashboards to grafana. 
Add the prometheus datasource to grafana.
```

# Accessing services

Grafana: 10.193.14.78:3000

Prometheus: 10.193.14.79:9090

# Notes

This project is an simplify example of the current stack. You will need to change the files to match your environment and system. 

If you need any help pelase open an issue, and I will try to help you making this work. 

This stack is currently working with +500 hosts, running the ceph_exporter, node_exporter, lustre_exporter, gpu_exporter, ...
