# Devbox
一个跨平台开箱即用的开发环境工具箱: once build, code every where。

## Feature list
- Redis
- Mysql
- Postgresql
- Rabbitmq

## 预安装工具
使用本项目前，请先确保你已经安装了 vagrant，如何安装？请看[这里](https://www.vagrantup.com/docs/installation)
当然，如果你是 mac 或者 win 用户，可以直接看下面 👇

### MacOS
``` bash
# 安装 homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# 安装 virtualbox vagrant
brew cask install virtualbox vagrant
```

### windows
1. 安装 chocolatey: https://chocolatey.org/install
2. 运行 `choco install vagrant virtualbox`

## 使用
本项目通过 vagrant + docker + shell script 的形式管理服务, 以下命令默认在 Devbox 根目录下运行

### 启动
启动: `vagrant up`
修改配置文件后，重启: `vagrant reload`

### 关闭
`vagrant destroy`

### 销毁
`vagrant halt`

### 管理服务
对服务的管理都需要在虚拟机下运行，因此在管理服务之前，必须通过 `vagrant ssh` 进入虚拟机

以 mysql 为例，创建一个数据库:
1. `vagrant ssh`
2. `sudo ./manage.sh mysql createdb <db name>`

更多示例请参考: `./docs/manage/*.md`

## Todo list
- [] 基础功能（服务安装/启停/创建资源等）
- [] 中文文档、示例
- [] 配置优化
- [] 添加更多服务
- [] 英文文档

## 资料
如果你想更进一步了解 vagrant、docker 这些技术，下面这些资料你可能会感兴趣 👇
- [Vagrant 文档 - 中文](https://tangbaoping.github.io/vagrant_doc_zh/v2/)
- [Vagrant 官方文档 - 英文](https://www.vagrantup.com/docs)
- [docker 文档 - 中文](https://docker-doc.readthedocs.io/zh_CN/latest/)
- [docker 官方文档 - 英文](https://docs.docker.com/)
