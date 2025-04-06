# serv00-xray

## socks

修改二进制文件名字，伪装为其他服务，作为cloudflare的proxyip

解决使用cloudflare workers edgetunnel项目导致托管在cloudflare的网站无法访问的问题

### how to use?


- 新建站点，找到serv00所在的ip
- 开启可执行权限
- 开放一个tcp端口
- 替换 `config` 的端口
- 修改用户名和密码


```shell
mkdir -p $HOME/domains/hugo
cd $HOME/domains/hugo
git https://github.com/esugarx/serv00-xray.git .
chmod +x ./hugo
./hugo -c ./config.json
```

配置edgetunnel项目，设置socks5代理即可