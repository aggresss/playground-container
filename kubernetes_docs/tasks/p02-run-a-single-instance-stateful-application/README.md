
https://kubernetes.io/docs/tasks/run-application/run-single-instance-stateful-application/

```
kubectl apply -f ./mysql-pv.yaml
kubectl apply -f ./mysql-deployment.yaml
kubectl describe pod mysql-
kubectl exec -it <pod-name> -- /bin/bash
    mysql -u root -p
        use mysql;
        update user set host = '%' where user = 'root';
        flush privileges;
        select host, user from user;
kubectl run -it --rm --image=mysql:latest --restart=Never mysql-client -- mysql -h mysql -p
kubectl delete deployment,svc mysql
kubectl delete pvc mysql-pv-claim
kubectl delete pv mysql-pv-volume
```