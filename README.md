#集群部署配置
```

#手动设置了容器的秘钥，容器拉取失败后更新秘钥文件
kubectl -n production create secret docker-registry ali-docker-token \
    --docker-server=registry.cn-beijing.aliyuncs.com \
    --docker-username=xxxx \
    --docker-password="xxxx" \
    --docker-email=xxxx@xxxx.com

#配置默认规则,将密钥设置到默认账号中
kubectl -n production patch serviceaccount default -p '{"imagePullSecrets": [{"name": "ali-docker-token"}]}'

#查看默认账号配置
kubectl -n production get serviceaccounts  default -o yaml





