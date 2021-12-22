# ingress-nginx

Ingress controller for Kubernetes using NGINX as a reverse proxy and load balancer

**Customized values**
```console
In Values.yaml file:
controller.ingressClassResource.name: namespace-ingress-class
controller.service.type: NodePort
controller.kind: DaemonSet
controller.service.nodePorts.http: allocated-http-port
controller.service.nodePorts.http: allocated-https-port
```
This chart bootstraps an ingress-nginx deployment on a Kubernetes cluster using the helm package manager.


## Setup Ingress Controller

**Important:** only helm3 is supported
```console
1. Clone the git repository
2. Authenticate to the cluster. Export the kubeconfig file
    export KUBECONFIG="config-file-path"
3. Deploy the application using helm chart present in the current repo:
    helm install nginx-ingress-contoller [current-repo-name] -n [namepsace]
```
## Upgrading Chart

```console
helm upgrade nginx-ingress-contoller [current-repo-name] -n [namepsace]
```
## Uninstalling Chart
```console
helm uninstall nginx-ingress-contoller -n [namepsace]
```