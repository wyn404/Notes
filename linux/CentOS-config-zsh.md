```
# 安装zsh
yum -y install zsh git

# 更改默认终端
chsh -s /bin/zsh

# 配置oh-my-zsh
git clone https://gitee.com/mirrors/oh-my-zsh.git ~/.oh-my-zsh

# 默认配置
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# 安装高亮插件
git clone https://gitee.com/dawnwords/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# 安装自动补全插件
git clone https://gitee.com/lhaisu/zsh-autosuggestions.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# 安装autojump目录跳转
cd ~/.oh-my-zsh/custom/plugins/ 
git clone https://gitee.com/gentlecp/autojump.git
cd autojump
./install.py


vim ~/.zshrc
...
source ~/.zshr
```
