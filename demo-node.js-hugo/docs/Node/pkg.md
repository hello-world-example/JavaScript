# pkg 打可执行文件



## 安装

```bash
$ npm install -g pkg
```



## 缓存目录

```bash
$ mkdir -p /opt/Commons/Node/pkg/Cache

$ sudo vim /etc/profile.d/node.sh
export PKG_CACHE_PATH=/opt/Commons/Node/pkg/Cache

# 生效
$ . /etc/profile

# 校验
$ echo $PKG_CACHE_PATH
```



## Hello World

### index.js

```js
console.info("Hello World !")
```

### 打包

```bash
# 去掉 -t macos 是所有平台，这里只打 MAC 平台
$ pkg -t macos index.js


# 成功后
$ ls
index        index.js
```

### 执行效果

```bash
# 执行
$ ./index
Hello World
```



## package.json 方式

### package.json 内容

> - `"bin": "index.js"` ： 入口文件
> - `pkg.scripts` ： 需要打包进来的 js 文件
> - `pkg.assets` ： 静态文件的目录

```json
{
  "name": "demo-node-pkg",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",

  "bin": "index.js",
  "pkg": {
    "scripts": [
      "build/**/*.js"
    ],
    "assets": [
      "dist/**/*"
    ]
  }
}
```

### 打包

```bash
$ pkg -t macos .

$ ls
demo-node-pkg   index.js       package.json

$ ./demo-node-pkg
Hello World
```



## Read More

- [vercel/pkg: Package your Node.js project into an executable (github.com)](https://github.com/vercel/pkg)
- [pkg - npm (npmjs.com)](https://www.npmjs.com/package/pkg)