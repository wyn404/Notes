配置Anaconda源

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/ 
conda config --set show_channel_urls yes
```

创建新环境

```
conda create -n name
conda create --name name python=x.x
```

查看当前conda所有环境

```
conda info --envs
conda info -e
```

激活环境

```
conda activate name
source activate name
activate name
```

退出当前环境

```
conda deactivate
```

删除环境

```
conda remove -n name
conda remove --name name --all
```

复制虚拟环境到新环境

```
conda create --name new_name --clone old_name
```





cmd进入anaconda prompt环境

```
conda.bat activate
```

临时镜像

```
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple/
```

永久镜像

```
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

