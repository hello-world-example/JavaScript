# Vue-Cli 快速入门

> 官方文档： https://cli.vuejs.org/zh/

## 安装

```bash
ᐅ npm install -g @vue/cli
# 检查是否安装正确
ᐅ vue --version
@vue/cli 4.1.1

ᐅ npm install -g @vue/cli-service-global
```



## hello-world

```bash
# 创建一个 hello-world 项目
ᐅ vue create hello-world

ᐅ cd hello-world
ᐅ npm run serve

# 详情查看 hello-world/README.md
```

### 单独查看组件

```bash
# 查看整个应用
ᐅ vue serve src/App.vue

# 查看 HelloWorld 组件
ᐅ vue serve src/components/HelloWorld.vue
```

## vue ui 图形化界面创建项目

> 如果本地无法测试，可以从[官网查看效果]([https://cli.vuejs.org/zh/guide/creating-a-project.html#%E4%BD%BF%E7%94%A8%E5%9B%BE%E5%BD%A2%E5%8C%96%E7%95%8C%E9%9D%A2](https://cli.vuejs.org/zh/guide/creating-a-project.html#使用图形化界面))

```bash
ᐅ vue ui
```



## Read More

- 官方文档 [创建一个项目](https://cli.vuejs.org/zh/guide/creating-a-project.html)