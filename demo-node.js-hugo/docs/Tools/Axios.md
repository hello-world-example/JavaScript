# Axios

> - 官网：https://github.com/axios/axios
> - 中文文档： https://www.kancloud.cn/yunye/axios/234845

## 基本语法结构

### try...catch...

```javascript
axios.get('/user?ID=12345')
    .then(function (response) { ... })
    .catch(function (error) { ... });
```

### GET 参数

```javascript
axios.get('/user', {
    params: {
        ID: 12345
    }
})
```

###  POST 参数
```javascript
axios.post('/user', {
    firstName: 'Fred',
    lastName: 'Flintstone'
})
```

## instance 参数

### init

```javascript
var instance = axios.create({
    baseURL: 'https://some-domain.com/api/',
    timeout: 1000,
    headers: { 'X-Custom-Header': 'foobar' }
});
```

### config simple

```javascript
{
  baseURL: 'https://some-domain.com/api/',
  url: '/user',
  method: 'get', // 默认是 get
  // URL 参数
  params: {
    ID: 12345
  },
  // 请求主体被发送的数据
  data: {
    firstName: 'Fred'
  },
    
  // 自定义请求头
  headers: {'X-Requested-With': 'XMLHttpRequest'},
    
  // 请求超时的毫秒数(0 表示无超时时间)
  timeout: 1000,
    
  // 对于给定的HTTP 响应状态码是 resolve 或 reject  promise
  validateStatus: function (status) {
    return status >= 200 && status < 300; // 默认的
  },

  // 在向服务器发送前，修改请求数据
  transformRequest: [function (data) { return data; }],
  transformResponse: [function (data) { return data; }],

  // HTTP 基础验证，并提供凭据
  auth: {
    username: 'admin',
    password: 'admin'
  },

  // 服务器响应的数据类型，默认json，可以是 'arraybuffer', 'blob', 'document', 'text', 'stream'
  responseType: 'json',

  // `onUploadProgress` 允许为上传处理进度事件
  onUploadProgress: function (progressEvent) {
    // 对原生进度事件的处理
  },

  // `onDownloadProgress` 允许为下载处理进度事件
  onDownloadProgress: function (progressEvent) {
    // 对原生进度事件的处理
  },

  httpAgent: new http.Agent({ keepAlive: true }),
  httpsAgent: new https.Agent({ keepAlive: true }),

  // 代理服务器的主机名称和端口
  proxy: {
    host: '127.0.0.1',
    port: 9000,
    auth: : {
      username: 'admin',
      password: 'admin'
    }
  }
}
```

## 默认配置

### 全局

```javascript
axios.defaults.baseURL = 'https://api.example.com';
```

### 实例

```javascript
var instance = axios.create({
  baseURL: 'https://api.example.com'
});

// 在实例已创建后修改默认值
instance.defaults.baseURL = 'https://api.example.com';
```

