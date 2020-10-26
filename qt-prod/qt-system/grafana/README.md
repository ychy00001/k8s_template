#1.创建阿里云云盘
#2.执行grafana-pv 中id需要替换云盘具体id
```
kubectl create -f grafana-pv.yaml
```
#3.执行grafana-pvc 中id需要替换云盘具体id
```
kubectl -n qt-system create -f grafana-pvc.yaml
```
#4.执行job任务
```
kubectl -n qt-system apply -f grafana-chown-job.yaml
```
#5.启动grafana
```
kubectl -n qt-system apply -f grafana-deploy.yaml
```
#5.创建service
```
kubectl -n qt-system apply -f grafana-svc.yaml
```
#6.创建ingress
```
kubectl -n qt-system apply -f grafana-ingress.yaml
```