# k8s

```bash
kubectl apply -f https://raw.githubusercontent.com/ShubhamTatvamasi/k8s/master/ibm.yaml
```
```bash
kubectl set image po ubuntu ubuntu=ubuntu:16.04
```
```bash
kubectl exec -it ubuntu -- bash
```
```bash
tail /root/ibm/var/log/syslog -f
```
```bash
kubectl delete po ubuntu
```
