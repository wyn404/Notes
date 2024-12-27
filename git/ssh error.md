错误描述：

```
ssh: Could not resolve hostname github.com: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

解决：

- windows：

1. 查找github.com网站的ip地址，https://myssl.com/dns_check.html#dns_check，进入网站后输入github.com查找ip地址
2. 使用管理员身份打开记事本，打开C:\Windows\System32\drivers\etc目录下的hosts文件

- linux

  sudo vim /etc/hosts

  末行加入20.205.243.166 github.com