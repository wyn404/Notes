### windows环境下git bash配置oh-my-zsh

##### 一、首先下载git

git官网[https://git-scm.com/](https://git-scm.com/)

##### 二、安装zsh

```
# 检查zsh版本，确认是否安装zsh
zsh --version

# 若未安装，先安装zsh
zsh安装包地址：https://packages.msys2.org/package/zsh?repo=msys&variant=x86_64
```

下载完成后，将下载后的文件etc,usr,.INSTALL,...等复制粘贴到Git目录下。

##### 三、Git Bash 安装 oh-my-zsh

1. 检查curl是否安装

```
curl --version
```

​	curl安装

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```



2. 手动安装

- 浏览器访问oh-my-zsh安装脚本


```
https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
```

- 手动创建oh-my-zsh的安装脚本：ohmyzsh_install.sh，将上一步的内容全部复制到ohmyzsh_install.sh中，然后执行此安装脚本即可安装oh my zsh


```
vim ~/.ohmyzsh_install.sh

sh ohmyzsh_install.sh
```



##### 四、Git Bash 配置 oh-my-zsh

要配置oh my zsh，通过编辑文件.zshrc来实现，在.zshrc中配置主题，插件等。

1. ###### 修改主题

编辑.zshrc中的ZSH_THEME参数即可修改zsh主题。

```
ZSH_THEME="***"

***可在https://github.com/ohmyzsh/ohmyzsh/wiki/Themes中挑选。
```

###### 	2. 安装zsh内置插件

编辑.zshrc中的plugins参数即可设置插件

```
plugins=(
	git
	docker
	...
)

# 插件存在位置
cd ~/.oh-my-zsh/plugins

# 访问如下地址可以查看插件的文档说明
https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins
```



###### 	3. 下载安装第三方插件

- *fast-syntax-highlighting*：为zsh提供丰富的shell语法高亮显示。
- **zsh-history-substring-search**：这是 Fish shell 历史搜索功能的简洁版实现，您可以通过ctrl + R开启搜索功能，键入历史中任何命令的任何部分，然后按选定的键（例如向上和向下箭头）以循环匹配历史命令。

- **zsh-autosuggestions**：可根据历史命令记录在您键入时提示命令。

以**fast-syntax-highlighting**为例，展示如何集成zsh插件。

首先，进入本地的oh my zsh源码目录，在plugins目录下通过git clone的方式下载第三方zsh插件。

```
cd ~/.oh_my_zsh/plugins

# clone the Repository
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting

# Add the following to your .zshrc file
和zsh内置插件安装步骤相同
```



###### 	4. git bash集成zsh插件

在~/.bashrc中添加如下命令，然后保存重启Git Bash即可。

```
# Launch Zsh
if [ -t 1 ]; then
    exec zsh
fi
```



##### 五、Git Bash上zsh中文乱码问题（重点）

在Git Bash上安装zsh和oh-my-zsh后，出现乱码的情况，请打开~/.zshrc文件，添加如下内容：

```
export LC_ALL=en_US.UTF-8
export LANG=en_US.UTF-8
```

保存后，执行如下命令即可解决乱码问题：

```
source ~/.zshrc
```

