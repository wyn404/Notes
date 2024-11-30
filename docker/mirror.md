修改daemon配置文件/etc/docker/daemon.json来使用加速器

```
sudo mkdir -p /etc/docker 

sudo v /etc/docker/daemon.json 

          {
       "registry-mirrors": [
          "https://2a6bf1988cb6428c877f723ec7530dbc.mirror.swr.myhuaweicloud.com",
          "https://docker.m.daocloud.io",
          "https://hub-mirror.c.163.com",
          "https://mirror.baidubce.com",
          "https://your_preferred_mirror",
          "https://dockerhub.icu",
          "https://docker.registry.cyou",
          "https://docker-cf.registry.cyou",
          "https://dockercf.jsdelivr.fyi",
          "https://docker.jsdelivr.fyi",
          "https://dockertest.jsdelivr.fyi",
          "https://mirror.aliyuncs.com",
          "https://dockerproxy.com",
          "https://mirror.baidubce.com",
          "https://docker.m.daocloud.io",
          "https://docker.nju.edu.cn",
          "https://docker.mirrors.sjtug.sjtu.edu.cn",
          "https://docker.mirrors.ustc.edu.cn",
          "https://mirror.iscas.ac.cn",
          "https://docker.rainbond.cc"
          ]
      }

sudo systemctl daemon-reload 

sudo systemctl restart docker
```

cat /etc/resolv.conf

```
新增nameserver 114.114.114.114和nameserver 8.8.8.8
```

