# GIT

> remote: Support for password authentication was removed on August 13, 2021.
fatal: Authentication failed fo ...

✅在 github/Settings/Developer Settings/Personal access tokens 生成一个tocken，再 `git remote set-url origin https://<token>@github.com/<name>/<repo_name>.git` ，连接到远程仓库。

</br>

> Failed to connect to github.com port 443: Connection refused

✅设置->网络和Internet->代理，查看**本机系统端口号**：
![](https://moonpic.oss-cn-beijing.aliyuncs.com/tf-feb/202401151156379.png)

```bash
git config --global http.proxy 127.0.0.1:<your_port>

git config --global https.proxy 127.0.0.1:<your_port>
```

reference from https://blog.csdn.net/qq_40296909/article/details/134285451
# Linux

## 下载源

**清华源**

`/etc/apt/sources.list`
```bash
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse

# 预发布软件源，不建议启用
# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
```

```bash
sudo apt-get update
sudo apt-get upgrade
```

**使用豆瓣源**

```bash
cd /home/user/
mkdir .pip
vim pip.conf
```

```bash
[global]
index-url = http://pypi.douban.com/simple
[install]
trusted-host = pypi.douban.com
```

**阿里源**

```bash
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
```


