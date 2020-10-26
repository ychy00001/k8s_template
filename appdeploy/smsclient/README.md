docker build -t smsclient .
docker tag smsclient registry.cn-beijing.aliyuncs.com/qingtengcloud/deploytest:smsclient1
docker push registry.cn-beijing.aliyuncs.com/qingtengcloud/deploytest:smsclient1
k -n deploytest apply -f smsclient.yaml

目录中的jar是不可用的 模拟jar包 
