## Ingress Controller 
An [Ingress controller](https://docs.nginx.com/nginx-ingress-controller/installation/installing-nic/installation-with-helm/) is a specialized load balancer for Kubernetes (and other containerized) environments. For many enterprises, moving production workloads into Kubernetes brings additional challenges and complexities around application traffic management. An Ingress controller abstracts away the complexity of Kubernetes application traffic routing and provides a bridge between Kubernetes services and external ones.
Kubernetes Ingress controllers:
- Accept traffic from outside the Kubernetes platform, and load balance it to pods (containers) running inside the platform
- Can manage egress traffic within a cluster for services which need to communicate with other services outside of a cluster
- Are configured using the Kubernetes API to deploy objects called “Ingress Resources”
- Monitor the pods running in Kubernetes and automatically update the load‑balancing rules when pods are added or removed from a service


### Installing the Chart using Helm
##### Create namespace
```
kubectl create ns nginx-ingress
```
##### Install the chart
```
helm install my-release oci://ghcr.io/nginxinc/charts/nginx-ingress --version 1.1.3 -n nginx-ingress
```
##### Voila!
```
kubectl get po -n nginx-ingress
```

#### List Helm releases in specific namespace
```
helm list -n <namespace>
```

#### Upgrading the Chart using Helm
```
helm upgrade my-release oci://ghcr.io/nginxinc/charts/nginx-ingress --version 1.1.3 -n <namespace>
```

#### Uninstalling the Chart using Helm
```
helm uninstall my-release -n <namespace>
```

## Add an Ingress Rule Manifest
[Ingress Resource](https://kubernetes.io/docs/concepts/services-networking/ingress/): object with a set of routing rules. Ingress exposes ```HTTP``` and ```HTTPS``` routes from outside the cluster to services within the cluster

```
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: my-ingress
  namespace: <namespace> 
spec:
  rules:
  - host: "my-domain.xyz"
    http:
      paths:
      - pathType: Prefix
        path: "/"
        backend:
          service:
            name: <serviceName>
            port:
              number: 80
```

