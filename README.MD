## 🧸配置文件
```yaml
app:
  # 运行模式：生产环境留空(开发模式：debug)
  mode: ""
  # 运行端口
  port: 15000
```

## 🔍安装教程
默认后台信息【第一次运行需要先注册账户，没有默认账户】
- 登录地址：IP或域名:15000/#/login
- 注册地址：IP或域名:15000/#/register
- 后台地址：IP或域名:15000/#/admin


安装方式二、Docker启动
```shell
# 创建QLTools目录并进入
mkdir qltools && cd qltools

# Docker版本提供架构：amd64、arm64、arm-7
docker run --restart=always -itd --name QLTools -v $PWD/config:/QLTools/config -v $PWD/plugin:/QLTools/plugin -p 5800:15000 littlexing/qltools

# 更新步骤：后台点击更新，稍等5分钟左右。手动重启容器即可完成更新（如果更新失败，请删除容器和镜像，然后重新拉取镜像启动）
# 重启命令：docker restart QLTools
```
