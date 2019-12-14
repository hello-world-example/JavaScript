# 常用命令

## npm 参数

```bash
# 查看各个命令的简单用法
ᐅ npm -l
```



## npm help 查看命令帮助

```bash
ᐅ npm help

Usage: npm <command>

where <command> is one of:
    access, adduser, audit, bin, bugs, c, cache, ci, cit,
    clean-install, clean-install-test, completion, config,
    create, ddp, dedupe, deprecate, dist-tag, docs, doctor,
    edit, explore, fund, get, help, help-search, hook, i, init,
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

npm@6.13.4 /Users/kail/.npm-global/lib/node_modules/npm
```



## npm config 操作配置信息

```bash
# 查看所有配置
ᐅ npm config list [--json]
# 编辑配置
ᐅ npm config edit
```



## npm ls / list 查看依赖

```bash
# 查看安装在全局第一层的包
ᐅ npm ls -g --depth=0
```



## npm root 查看依赖安装目录

```bash
ᐅ npm root -g
/Users/kail/.npm-global/lib/node_modules
```



## npm info 查看包的详细信息

```bash
 ᐅ npm info npm

npm@6.13.4 | Artistic-2.0 | deps: 123 | versions: 336
a package manager for JavaScript
https://docs.npmjs.com/

bin: npm, npx

dist
.tarball: https://registry.npm.taobao.org/npm/download/npm-6.13.4.tgz
.shasum: 1e95b0f311999cf682384c38865dfeb3127203bb

dependencies:
JSONStream: ^1.3.5      aproba: ^2.0.0          byte-size: ^5.0.1       ci-info: ^2.0.0         columnify: ~1.5.4       dezalgo: ~1.0.3         
abbrev: ~1.1.1          archy: ~1.0.0           cacache: ^12.0.3        cli-columns: ^3.1.2     config-chain: ^1.1.12   editor: ~1.0.0          
ansicolors: ~0.3.2      bin-links: ^1.1.6       call-limit: ^1.1.1      cli-table3: ^0.5.1      detect-indent: ~5.0.0   figgy-pudding: ^3.5.1   
ansistyles: ~0.1.3      bluebird: ^3.5.5        chownr: ^1.1.3          cmd-shim: ^3.0.3        detect-newline: ^2.1.0  find-npm-prefix: ^1.0.2 
(...and 99 more.)

maintainers:
- adam_baldwin <baldwin@andyet.net>
- ahmadnassri <ahmad@codeinchaos.com>
- annekimsey <anne@npmjs.com>
- billatnpm <billatnpm@gmail.com>
- claudiahdz <cghr1990@gmail.com>
- darcyclarke <darcy@darcyclarke.me>
- isaacs <i@izs.me>
- mikemimik <mike@mikecorp.ca>
- ruyadorno <ruyadorno@hotmail.com>

dist-tags:
latest-1: 1.4.29   latest-3: 3.10.10  latest-5: 5.10.0   latest: 6.13.4     next-2: 2.15.12    next-4: 4.6.1      next-6: 6.13.4     
latest-2: 2.15.12  latest-4: 4.6.1    latest-6: 6.13.4   lts: 6.13.4        next-3: 3.10.10    next-5: 5.10.0     next: 6.13.4       

published 2 days ago by isaacs <i@izs.me>
```



## npm home 打开指定模块的主页

`package.json` > `"homepage"`

```bash
# 会跳到 https://docs.npmjs.com/
ᐅ npm home npm
```



## npm repo 打开指定模块的仓库

`package.json` > `"repository"`

```bash
# 会跳到 https://github.com/npm/cli
ᐅ npm repo npm
```



## Read More

- 阮一峰 [npm模块管理器](https://javascript.ruanyifeng.com/nodejs/npm.html)