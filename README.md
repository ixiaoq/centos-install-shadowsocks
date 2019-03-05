# Centos 安装 shadowsocks

请按照下面步骤进行安装。。

### 对系统进行更新，安装 wget
  ```bash
  yum -y update && yum -y install wget
  ```

### 安装SS，执行下面命令
  ```bash
  wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
  ```

### 赋予执行权限
  ```bash
  chmod +x shadowsocks.sh
  ```

### 执行安装并启动
  ```bash
  ./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
  ```
  
>（按照提示内容，设置对应的信息）


--------------------------------------- 安装完成 -----------------------------------------------



### 编辑配置文件
  ```bash
  nano /etc/shadowsocks-r/config.json
  ```
  
>更改完设置后,重启
  ```bash
  /etc/init.d/shadowsocks-r restart
  ```

### Shadowsocks服务器端提速优化
  ```bash
  wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
  ```