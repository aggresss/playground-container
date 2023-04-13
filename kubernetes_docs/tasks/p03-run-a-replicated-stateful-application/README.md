
- https://kubernetes.io/docs/tasks/run-application/run-replicated-stateful-application/

> The headless Service provides a home for the DNS entries that the StatefulSet controllers creates for each Pod that's part of the set. Because the headless Service is named mysql, the Pods are accessible by resolving <pod-name>.mysql from within any other Pod in the same Kubernetes cluster and namespace.

```
kubectl apply -f ./mysql-configmap.yaml
kubectl get configmaps mysql
kubectl apply -f ./mysql-services.yaml
kubectl apply -f ./mysql-statefulset.yaml

```