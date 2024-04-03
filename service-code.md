## 服务常用代码

我使用的是阿里云服务器（2 vCPU 2 GiB（ecs.e-c1m1.large）），Ubuntu@22.04 64位。文中所有例子都基于这个镜像系统。

### 镜像&系统选择

最好使用公共镜像，有新的就选新的。当然也可以选一些镜像市场提供的，比如说宝塔、LAMP

| 镜像名 | 推荐 | 包管理 | 市场占有 | 稳定性 |
| - | - | - | - | - |
| Ubuntu | ⭐️ | apt | - | - |
| CentOS | ⭐️ | yum | - | - |
| Debian | ⭐️ | apt | - | - |
| Alibaba Cloud Linux | - | - | - | - |
| Anolis OS | - | - | - | - |
| CentOS | - | - | - | - |
| Windows Server | - | - | - | - |
| SUSE Linux | - | - | - | - |
| Fedora | - | - | - | - |
| OpenSUSE | - | - | - | - |
| Rocky Linux | - | - | - | - |
| CentOS Stream | - | - | - | - |
| AlmaLinux | - | - | - | - |
| Fedora CoreOS | - | - | - | - |
| FreeBSD | - | - | - | - |


### 安装命令
#### [snapd](https://snapcraft.io/docs/installing-snapd)
```shell
sudo apt update
sudo apt install snapd

sudo snap install hello-world
hello-world
```

#### [certbot](https://certbot.eff.org/instructions?ws=nginx&os=arch)
```shell
sudo apt-get remove certbot
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
# sudo certbot --nginx
# sudo certbot renew --dry-run
# certbot --nginx --email lilnong1@126.com -d jgq-static.lilnong.top -d jgq-server.lilnong.top


```


#### [nvm](https://github.com/nvm-sh/nvm) 
```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

# OR
# wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```
#### [nginx](https://github.com/nginx/nginx) | [docs](https://nginx.org/en/docs/install.html)
```shell
# install the prerequisties
sudo apt install curl gnupg2 ca-certificates lsb-release ubuntu-keyring
sudo apt update
sudo apt install nginx
```

#### Node
```shell
nvm install 18
nvm use 18

npm install -g pm2 yarn pnpm

# code-server
curl -fsSL https://code-server.dev/install.sh | sh
```

#### mongodb
#### radis
#### mariadb

## 其他
1. [SF笔记](https://segmentfault.com/n/1330000023372599)