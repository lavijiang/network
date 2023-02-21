# network

# Install Shadowsocks
## 1. install docker engine
https://docs.docker.com/engine/install/ubuntu/

## 2. use ss image
https://github.com/shadowsocks/shadowsocks-libev/tree/master/docker/alpine

## 3. start
nohup sudo docker compose up >/dev/null 2>&1 &

  
# Install Trojan
## 1 官方教程
https://p4gefau1t.github.io/trojan-go/basic/trojan/  
在开始之前，你需要
- 一个服务器，且未被GFW封锁
- 一个域名，可以使用免费的域名服务，如.tk等
- Trojan-Go，可以从release页面下载
- 证书和密钥，可以从letsencrypt等机构免费申请签发

## 2 将域名解析和服务器ip绑定

## 3 在服务器上启动一个HTTP服务器
以ubuntu安装nginx为例
- 安装
```
sudo apt-get install nginx
```
- 启动
```
sudo service nginx start
```
- 查看
```
sudo service nginx status
```
- 查看nginx配置
```
cat /etc/nginx/nginx.conf
```
输入你的域名，如果出现nginx的页面就ok。nginx服务默认监听80端口，需要在云提供商放开80限制，或者使用其他端口。
