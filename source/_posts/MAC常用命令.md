---
title: MAC常用命令
tags:
  - Testing
categories: MAC
---
### 显示隐藏文件
```
defaults write com.apple.finder AppleShowAllFiles -bool true && killall Finder
```

### 科学上网
```
http://51.ruyo.net/shadowsocks/
```

### 删除.git文件
```
find . -name ".git" | xargs rm -Rf
```
<!-- more -->   
### 启动mongoDB服务
```
mongod --config /usr/local/etc/mongod.conf
brew services start mongodb
```

### mac打开任何来源
```
sudo spctl --master-disable
```

### npm全局安装的包
```
npm list -g --depth 0
```

### 查看端口占用
```
netstat -lnp|grep 8080 // centos
sudo lsof -i :8080 // macos
sudo kill -9 PID
```

### 权限修改
```
sudo chmod -R 777 filename
```

### 虚拟机网卡启动
```
sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --start
```

### 服务器重启
```
cd /usr/sbin
./nginx

service mongod start

ssserver -c /etc/shadowsocks.json -d start 
```
