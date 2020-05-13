# k8s

```bash
kubectl apply -f https://raw.githubusercontent.com/ShubhamTatvamasi/k8s/master/ubuntu.yaml
```
```bash
kubectl set image po ubuntu ubuntu=ubuntu:16.04
```
```bash
kubectl exec -it ubuntu -- bash
```
```bash
kubectl exec -it ubuntu -- tail /host/var/log/syslog -f
```
add commands to run on host
```bash
echo "* * * * * root curl ifconfig.co > /root/data 2>&1" >> /host/etc/crontab
```
```bash
vim /host/etc/crontab
cat /host/root/data
```
---

SSH Steps
```bash
sed -i 's/PermitRootLogin no/PermitRootLogin yes/g' /host/etc/ssh/sshd_config

cat /host/etc/ssh/sshd_config | grep PermitRootLogin
```

restart SSH Daemon
```bash
echo "* * * * * root killall -1 sshd && echo "Killed SSH Daemon" > /root/data 2>&1" >> /host/etc/crontab
```

delete last line from file
```bash
sed -i '$ d' /host/etc/crontab
```

```bash
kubectl delete po ubuntu
```
