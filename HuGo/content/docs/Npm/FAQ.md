# 常见问题

## 使用国内镜像

> npm registry 管理： https://www.jianshu.com/p/2f532f8f2e19
>

```bash
# 安装「npm install -g nrm --registry=https://registry.npm.taobao.org」
ᐅ npm install -g nrm

# 查看支持的镜像
ᐅ nrm ls
  npm -------- https://registry.npmjs.org/
  yarn ------- https://registry.yarnpkg.com/
  cnpm ------- http://r.cnpmjs.org/
  taobao ----- https://registry.npm.taobao.org/
  nj --------- https://registry.nodejitsu.com/
  npmMirror -- https://skimdb.npmjs.com/registry/
  edunpm ----- http://registry.enpmjs.org/
  
# 切换为 淘宝镜像
ᐅ nrm use taobao
   Registry has been set to: https://registry.npm.taobao.org/

# 查看效果
ᐅ npm config get registry
https://registry.npm.taobao.org/
```



## 权限问题

> 处理npm权限问题 ： https://www.kancloud.cn/shellway/npm-doc/199985
>
> 这里使用第二种方法

```bash
# 查看 npm 的目录路径
ᐅ npm config get prefix
/usr/local

# 为 npm 设置新路径
ᐅ mkdir ~/.npm-global
ᐅ npm config set prefix '/Users/kail/.npm-global'
# 追加 export PATH="$PATH:/Users/kail/.npm-global/bin"
ᐅ sudo vim /etc/profile
ᐅ source /etc/profile

# 测试效果
ᐅ npm install -g npm
ᐅ npm install -g --force npx
ᐅ npm ls -g --depth=0       
/Users/kail/.npm-global/lib
├── npm@6.13.4
└── npx@10.2.0

# 删除原有 node_modules
ᐅ sudo rm -rf /usr/local/lib/node_modules
```

