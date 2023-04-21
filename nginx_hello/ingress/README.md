
- https://kubernetes.github.io/ingress-nginx/
- https://kubernetes.github.io/ingress-nginx/deploy/
- https://kubernetes.github.io/ingress-nginx/deploy/#quick-start
- https://www.infoq.cn/article/vl7SZGQc2JUaM6IisAhE


There are multiple ways to install the NGINX ingress controller:

- with Helm, using the project repository chart;
- with kubectl apply, using YAML manifests;
- with specific addons (e.g. for minikube or MicroK8s).

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/mandatory.yaml
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.7.0/deploy/static/provider/cloud/deploy.yaml

```
