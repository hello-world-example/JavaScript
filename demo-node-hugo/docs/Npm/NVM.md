# nvm 管理 Node 版本

> 如果使用 nvm 管理 node 版本，需要先卸载已经安装的 node 和 npm，否则切换版本的时候可能会报一下错误：
>
> > nvm is not compatible with the npm config "prefix" option: currently set to "xxx"

## 卸载已安装的 node & npm

```bash
# 查看已经安装在全局的模块，便于重新安装
ᐅ npm ls -g --depth=0
└── xxx

# 删除 node
ᐅ sudo rm /usr/local/bin/node
ᐅ sudo rm /usr/local/bin/npm
ᐅ sudo rm /usr/local/bin/npx
ᐅ sudo rm -rf /usr/local/lib/node_modules

ᐅ rm ~/.npmrc
ᐅ rm ~/.nrmrc
ᐅ rm -rf ~/.npm
ᐅ rm -rf ~/.node-gyp
ᐅ rm -rf ~/.npm-global
```

## 官方安装方式

> 官网：https://github.com/nvm-sh/nvm/

```bash
ᐅ wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
```

## 手动安装方式

```bash
ᐅ git clone https://gitee.com/mirrors/nvm.git ~/.nvm
ᐅ cd ~/.nvm
ᐅ git remote set-url origin https://github.com/nvm-sh/nvm.git
ᐅ git pull
ᐅ git checkout `git describe --abbrev=0 --tags`

# 编辑 /etc/profile，追加已下代码
ᐅ sudo vim /etc/profile
# nvm
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
# nvm 国内镜像
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node

ᐅ source /etc/profile
```

## 使用 nvm

```bash
# 查看有哪些可用版本
ᐅ nvm ls-remote --lts

# 安装指定版本
ᐅ nvm install v12.21.0

# 查看本地版本
ᐅ nvm ls --no-alias

# 切换到指定版本
ᐅ nvm use v12.21.0

# 显示当前版本
ᐅ nvm current

# 设置默认版本
ᐅ nvm alias default v12.21.0

# 显示当前版本安装的全局包
ᐅ npm ls -g --depth=0
/Users/kail/.nvm/versions/node/v8.17.0/lib
└── npm@6.13.4
```
