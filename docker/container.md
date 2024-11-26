
docker pull xxxxxx # 拉取镜像（hub.docker.com）

docker images # 查看已下载镜像

docker ps -a # 查看已创建的容器

docker start xxxxxx # 开启容器

docker run -it image-id /bin/bash # 创建容器

docker run -itd --name xxx -v /host-path:/workspace --privileged=true --network=host image-id # 将主机文件映射到容器中

docker exec -it container-id /bin/bash #进入容器

docker rm container-id # 删除容器



#### linux环境下docker运行时无须前加sudo
'''
     sudo usermod -aG docker $USER
    sudo systemctl restart docker
    newgrp docker
'''
