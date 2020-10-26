#网关构建内容

相关命令：
```
kubectl -n development apply -f development-dft-gateway.yaml

#生产环境应用网关
kubectl -n production apply -f production-dft-gateway.yaml
```

#创建SDS使用的credential
> ingress-gateway需要开启sds支持
```

kubectl create -n qt-app secret generic xxx-credential \
--from-file=key=xxx.key \
--from-file=cert=xxx.pem

```