首先，创建一个容器，并进入

```
sudo docker run -itd --name name -v /home/wyn/xxx:/workspace --privileged=true --gpus all -p 10022:22 --ipc=host image-id

sudo docker exec -it test /bin/bash
```

在容器内进行对应配置

```
apt update

apt install -y openssh-server

mkdir /var/run/sshd
echo 'root:1212' | chpasswd
sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
sed 's@session\s*required\s*pam_loginuid.so@session optional pam_loginuid.so@g' -i /etc/pam.d/sshd
echo "export VISIBLE=now" >> /etc/profile
```

重启ssh

```
service ssh restart
```

ssh连接

```
sudo docker start contain-id/name
sudo docker port contain-id/name

ssh root@ip -p 22
```



查看docker内主机ip

```
hostname -i
```

报错：Permission denied (publickey,password)

```
docker exit -it ...
vim /etc/ssh/sshd_config

修改PermitRootLogin yes
```

