# 迅速測試環境架設指南

## 概念
- 運用docker-compose實現環境迅速架設與獨立化
- 

## 需要環境
- Linux系統(建議Ubuntu)
- docker(建議：18.03.1-ce 以上)
- docker-compose(建議：21 以上)

### 環境包含
- jupyter notebook(可在Host瀏覽器 localhost:8888啟用)
  - container name: jupyter.local
- mysql
  - container name: bb106db

### docker環境概念
- [網路概念](../docker_network.pdf)



## 環境建立

### docker-ce安裝
- 不論是Ubuntu或者CentOS內建都是docker 1.13，此版本太舊，建議換新
- 安裝指令：
``` sh 
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu xenial stable"
sudo apt-get update

apt-cache search docker-ce
sudo apt-get install docker-ce

```
- [參考網站](https://unix.stackexchange.com/questions/363048/unable-to-locate-package-docker-ce-on-a-64bit-ubuntu)


### docker-compose安裝
- 安裝指令：
``` sh
sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version

```

### docker-compose迅速建立環境
- [docker-compose.yml file](docker-compose.yml)
- cd 到包含docker-compose.yml的目錄
- 運行指令：`docker-compose up`
  - `docker-compose up -d`：所有容器背景運行，不會看到log(生產環境使用)
  - `docker-compose up`：所有容器的log顯示於同一個終端視窗，方便測試時使用










