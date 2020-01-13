# verdaccio

记录 verdaccio 基于docker-compose私有部署的配置

# 碰到问题

1. 找不到 config.yaml 配置文件（[docker-compose] cannot open config）
   [碰到的问题描述和解决方法，看这个issues](https://github.com/verdaccio/docker-examples/issues/30)
2. 目录文件操作权限，例如

- EACCES: permission denied, open '/verdaccio/conf/htpasswd'
- EACCES: permission denied, open '/verdaccio/storage/.sinopia-db.json'"
- EACCES: permission denied, mkdir '/verdaccio/storage/toolkit'
  
  > 解决方法： > sudo chown 10001:65533 verdaccio（宿主机映射目录）

