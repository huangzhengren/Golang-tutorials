[TOC]


# Install Golang on Linux

```shell
[root@app01 software]# wget https://studygolang.com/dl/golang/go1.16.2.linux-amd64.tar.gz
[root@app01 software]# tar -zxvf go1.16.2.linux-amd64.tar.gz -C /usr/local
[root@app01 software]# echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/profile
[root@app01 software]# source /etc/profile
[root@app01 software]# go version
```

# Golang environment configuration

```shell
[root@app01 software]# go env
[root@app01 software]# go env -w GO111MODULE="on"
[root@app01 software]# go env -w GOPROXY="https://goproxy.cn,direct"
```

