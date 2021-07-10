# 快速开始



## 安装

```bash
$ npm install -g yarn

# 
# $ npm install -g tyarn
```



## 常用指令

### install 安装依赖

```bash
$ yarn

$ yarn install
```



### 添加依赖项

```bash
# 默认添加到 dependencies 节点
$ yarn add [package]
$ yarn add [package]@[version]
$ yarn add [package]@[tag]
```



### 将依赖项添加到不同的依赖类别中

```bash
# devDependencies
$ yarn add [package] --dev

# peerDependencies
$ yarn add [package] --peer
```



### 更新依赖项

```bash
$ yarn up [package]
$ yarn up [package]@[version]
$ yarn up [package]@[tag]
```



### 删除依赖项

```bash
$ yarn remove [package]
```



### 更新 yarn 本体

```bash
$ yarn set version latest
$ yarn set version from sources
```



### 其他

```bash
# 命令帮助
$ yarn help
$ yarn -h
$ yarn --help

# 初始化项目
$ yarn init
```









## Read More

- [Usage | Yarn (yarnpkg.com)](https://classic.yarnpkg.com/en/docs/usage)
- [CLI Introduction | Yarn (yarnpkg.com)](https://classic.yarnpkg.com/en/docs/cli/)