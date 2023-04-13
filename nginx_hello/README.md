
## Reference

- https://docs.olcf.ornl.gov/services_and_applications/slate/use_cases/nginx_hello_world.html
- https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-ingress-guide-nginx-example.html
- https://platform9.com/learn/v1.0/tutorials/nginix-controller-via-yaml
- https://docs.oracle.com/en-us/iaas/Content/ContEng/Tasks/contengdeployingsamplenginx.htm
- https://blog.csdn.net/weixin_45710811/article/details/126256165
- https://www.cnblogs.com/vincegod/p/16101797.html

```
kubectl create deployment hello-nginx --image=nginx --replicas=2
kubectl expose deployment hello-nginx --port=8001 --target-port=80 --type=NodePort
kubectl expose deployment hello-nginx --port=8001 --target-port=80 --type=ClusterIP
kubectl get service
```

- 集群内部可以通过 8001 访问
- http://localhost:<nodePort>
- 下面示例中 nodePort=32192, port=8001, targetPort=80

```
kubectl get service
NAME          TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
hello-nginx   NodePort    10.109.202.252   <none>        8001:32192/TCP   158m
kubernetes    ClusterIP   10.96.0.1        <none>        443/TCP          3d9h
```

```
kubectl get service
NAME          TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
hello-nginx   ClusterIP   10.101.93.106   <none>        8001/TCP   3s
kubernetes    ClusterIP   10.96.0.1       <none>        443/TCP    3d9h
```