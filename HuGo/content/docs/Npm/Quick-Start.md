

# npm 快速入门

> - npm 官网：https://www.npmjs.com/
> - npm 中文文档： https://www.npmjs.cn/
>   - [快速入门](https://www.npmjs.cn/getting-started/what-is-npm/)

## 简介

NPM（Node Package Manager）

- 查找包：https://www.npmjs.com/search?q=qrcode

## 安装 Node & npm

> Node 官网：https://nodejs.org/en/download/
>
> 目前新版 Node，内置 npm 「 Latest LTS Version: **12.13.1** (includes npm 6.12.1) 」
>
> 安装过程 “点点点” 即可

```bash
# Node 版本
ᐅ node -v
v12.13.1
# npm 版本
ᐅ npm -v
6.12.1

# 使用帮助
ᐅ npm help

Usage: npm <command>

where <command> is one of:
    access, adduser, audit, bin, bugs, c, cache, ci, cit,
    clean-install, clean-install-test, completion, config,
    create, ddp, dedupe, deprecate, dist-tag, docs, doctor,
    edit, explore, get, help, help-search, hook, i, init,
    install, install-ci-test, install-test, it, link, list, ln,
    login, logout, ls, org, outdated, owner, pack, ping, prefix,
    profile, prune, publish, rb, rebuild, repo, restart, root,
    run, run-script, s, se, search, set, shrinkwrap, star,
    stars, start, stop, t, team, test, token, tst, un,
    uninstall, unpublish, unstar, up, update, v, version, view,
    whoami

npm <command> -h  quick help on <command>
npm -l            display full usage info
npm help <term>   search for help on <term>
npm help npm      involved overview

Specify configs in the ini-formatted file:
    /Users/kail/.npmrc
or on the command line via: npm <command> --key value
Config info can be viewed via: npm help config

npm@6.12.1 /usr/local/lib/node_modules/npm
```

## * nvm 管理 Node & npm 版本

> 官网：https://github.com/nvm-sh/nvm/



## 常用命令

### install

```bash
# 本地安装
ᐅ npm install <package-name>@<version>
# 全局安装
ᐅ npm install -g <package-name>@<version>

# 表示将这个包名及对应的版本添加到 package.json 的 dependencies
ᐅ npm install <package-name> --save 
# 表示将这个包名及对应的版本添加到 package.json 的 devDependencies
ᐅ npm install <package-name> --save-dev 

# 查看 package.json 中定义的依赖是否有新版本
ᐅ npm outdated
# 更新指定依赖
ᐅ npm update <package-name>

# 查看使用帮助
ᐅ npm help install
```



### uninstall

```bash
# 卸载一个依赖
ᐅ npm uninstall <package-name>
```



