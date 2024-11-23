修改daemon配置文件/etc/docker/daemon.json来使用加速器

```
sudo mkdir -p /etc/docker 

sudo tee /etc/docker/daemon.json <<-'EOF' 

{  
	"registry-mirrors": [
        "https://3d9cyf7l.mirror.aliyuncs.com"，
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
EOF 

sudo systemctl daemon-reload 

sudo systemctl restart docker
```

