```bash
kubectl create ns nginx
kubectl run nginx --image=nginx -n nginx
kubectl delete pod nginx -n nginx
kubectl delete ns nginx
```
```bash
kubectl apply -f namespace.yml  
kubectl create -f namespace.yml --save-config
kubectl apply -f pod.yml
kubectl exec -it pod/nginx-pod -n nginx -- bash
kubectl scale deployment/nginx-deployment --replicas=1 -n nginx
```