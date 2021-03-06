***本项目在 CentOS 7.6 环境下开发***
</br>

## 🔧 脚本用法
- 本项目中的各脚本，请在 `/root/` 目录以外的任意普通目录执行，否则部分脚本无法执行成功，建议 `/data/` 目录（虽然大部分脚本在 `/root/` 目录也能执行成功）。  
- 对于需要下载包的脚本，都提供了在线和离线安装的方法。离线安装的话，只需要将脚本和下载包放在同一目录即可。  
- 如果在离线环境下部署依赖于 `yum` 等工具，需要在线下载部署的，可使用以下命令将rpm包下载到本地后离线安装。  
```shell
yum install --downloadonly --downloaddir=/data/xxxpackage/ 包名  
cd /data/xxxpackage/
rpm -Uvh ./*rpm
```
</br>

> 项目致力于实现一键部署各种常见服务，实现常用功能，且具有幂等性（多次执行效果一致）的脚本具有，如果发现有bug，请提 issues 🙋‍♂️

## 📚 目录结构
```shell
.
├── 01-installation-scripts
│   ├── 01-MySQL
│   ├── 02-Zabbix
│   ├── 03-Jumpserver
│   ├── 04-Docker
│   ├── 05-Jenkins
│   ├── 06-Gitlab
│   ├── 07-Nginx-tengine-openresty-kong
│   ├── 08-EFK
│   ├── 09-Redis
│   ├── 10-GoAccess
│   ├── 11-vsftp
│   ├── 12-MongoDB
│   ├── 13-jdk
│   ├── 14-zookeeper
│   ├── 15-maven
│   ├── 16-kafka
│   ├── 17-rabbitmq
│   └── 18-Elasticsearch
├── 02-elasticsearch-tools
│   ├── 01-clean-single-es-index-by-date.sh
│   └── 02-clean-date-format-es-index-by-date.sh
├── 03-Dockerfile
│   ├── 01-nacos
│   ├── 02-feely-sys
│   └── 03-centos
├── 04-disk-tools
│   ├── 01-Create-Swap
│   └── 02-Create-LVM
├── 05-system-tools
│   ├── 01-check-package-manager.sh
│   ├── 02-update-openssh.sh
│   └── 03-init-system.sh
├── 06-Antivirus-tool
│   └── 01-kill_miner_proc.sh
└── README.md

```
