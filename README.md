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


