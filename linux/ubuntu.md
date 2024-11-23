切换root用户

```
su 
```



root用户、docker环境终端彩色

文件：/etc/bash.bashrc，~/.bashrc

```
#shell color style setting 
 
export PS1="\[\e[36m\]\u\[\e[m\]@\[\e[32m\]\h\[\e[m\]:\[\e[33m\]\w\[\e[m\]\$ " 
 
export GREP_OPTIONS='--color=auto' 
#export GREP_COLOR='1;35' 
alias grep='grep --color=always -i'
export GREP_COLOR="1;31"
alias ls='ls --color=auto' 
 
export LESS_TERMCAP_mb=$'\E[01;31m' 
export LESS_TERMCAP_md=$'\E[01;31m' 
export LESS_TERMCAP_me=$'\E[0m' 
export LESS_TERMCAP_se=$'\E[0m' 
export LESS_TERMCAP_so=$'\E[01;44;33m' 
export LESS_TERMCAP_ue=$'\E[0m' 
export LESS_TERMCAP_us=$'\E[01;32m'
```

