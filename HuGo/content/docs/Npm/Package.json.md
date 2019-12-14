# package.json

管理本地安装 npm 包的最好方式就是创建 `package.json` 文件。

## 创建 package.json

```bash
# 输入之后开始交互式操作，按提示进行即可
ᐅ npm init

# 直接生成默认的 package.json，之后修改文件
ᐅ npm init --yes
```

## package.json 内容

- ! `name`：项目名。全部小写，没有空格，可以使用下划线或者横线
- ! `version`：x.x.x 格式的版本号
- `description`：描述信息，有助于搜索，如果没定义，npm 使用项目中的 README.md 的第一行
- `main`: 入口文件，一般都是 `index.js`
- `scripts`：支持的脚本，默认是一个空的 test
- `keywords`：关键字，有助于在人们使用 `npm search` 搜索时发现你的项目
- `author`：作者信息
- `license`：默认是 [MIT](https://zh.wikipedia.org/wiki/MIT許可證)
- `bugs`：当前项目的一些错误信息，如果有的话

可以为 `init` 命令设置一些默认值，比如：

```
ᐅ npm set init.author.name "kail"
ᐅ npm set init.license "MIT"
```

## 版本依赖

- `devDependencies`：在开发、测试环境中用到的依赖
- `dependencies`：在生产环境中需要用到的依赖

`npm install` 默认会安装 `package.json` 中 `dependencies` 和 `devDependencies` 里的所有模块。

如果想只安装 `dependencies` 中的内容，可以使用 `--production` 字段：`npm install --production`

```javascript
{    
    "name": "xxx",
    "version": "x.x.x",
    "devDependencies": {
        "my_dep": "^1.0.0",
        "another_dep": "2.2.0"
    },
    "dependencies": {
        "my_dep": "^1.0.0",
        "another_dep": "~2.2.0"
    }
}
```



> 语义化版本规则： https://docs.npmjs.com/about-semantic-versioning

### 版本号规范

如果一个项目打算与别人分享，应该从 1.0.0 版本开始。以后要升级版本应该遵循以下标准：

- **补丁版本**：解决了 Bug 或者一些较小的更改，增加最后一位数字，比如 1.0.1
- **小版本**：增加了新特性，同时不会影响之前的版本，增加中间一位数字，比如 1.1.0
- **大版本**：大改版，无法兼容之前的，增加第一位数字，比如 2.0.0

### 可接受包的更新程度

- 如果**只打算接受补丁版本**的更新（也就是最后一位的改变），就可以这么写：
  - `1.0`
  - `1.0.x`
  - `~1.0.4`
- 如果**接受小版本**的更新（第二位的改变），就可以这么写：
  - `1`
  - `1.x`
  - `^1.0.4`
- 如果可以**接受大版本的更新**（自然接受小版本和补丁版本的改变），就可以这么写：
  - `*`
  - `x`

小结一下：**总共三种版本变化类型，接受依赖包哪种类型的更新，就把版本号准确写到前一位。**



## Read More

- 阮一峰 [package.json文件](https://javascript.ruanyifeng.com/nodejs/packagejson.html)

- [npm 与 package.json 快速入门](https://juejin.im/entry/598286cb6fb9a03c5b04a4ff)

  

