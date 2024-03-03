#### Overview
An Ingress controller is a specialized load balancer for Kubernetes (and other containerized) environments. For many enterprises, moving production workloads into Kubernetes brings additional challenges and complexities around application traffic management. An Ingress controller abstracts away the complexity of Kubernetes application traffic routing and provides a bridge between Kubernetes services and external ones.
Kubernetes Ingress controllers:
- Accept traffic from outside the Kubernetes platform, and load balance it to pods (containers) running inside the platform
- Can manage egress traffic within a cluster for services which need to communicate with other services outside of a cluster
- Are configured using the Kubernetes API to deploy objects called “Ingress Resources”
- Monitor the pods running in Kubernetes and automatically update the load‑balancing rules when pods are added or removed from a service
