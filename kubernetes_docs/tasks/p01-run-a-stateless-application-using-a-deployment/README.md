
https://kubernetes.io/docs/tasks/run-application/run-stateless-application-deployment/

```
kubectl apply -f deployment-update.yaml
kubectl get pods -l app=nginx
kubectl describe deployment nginx-deployment
kubectl delete deployment nginx-deployment
```