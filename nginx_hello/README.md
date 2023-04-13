
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
kubectl get service
```

集群内部可以通过 8001 访问
