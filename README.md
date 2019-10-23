# axios-package

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```
axios 简单封装 降低耦合
 src下 api文件夹是请求的总体文件，包含了 http(axios封装)，url 分类接口管理，api.js 是最终在页面上面调用的方法

文件顺序 ：
1、request.js   创建了一个axios请求类，设置了公共属性，和请求拦截
2、http.js   请求发出去的地方  get或者post
3、api.js    最终return一个对象
{
    login:function(params){
        <!-- url和method 是在url文件夹的method和url -->
        http(url,method,params)
    }
    ...
}
最终挂载在vue.prtotype.$http = http
在页面使用  如app.vue
### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
