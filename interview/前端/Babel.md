# Babel

Babel是一个将ES6语言转换为ES5或者ES4来保证所有语言都能被浏览器编译  
Babel配置说明：

配置

```json
{
    "name":"babel",
    "version":"1.0.0",
    "description":"",
    "main":"index.js",// the entry file
    "scripts":{
        "test":"echo \"Error: no test specified && exit 1",
    },
    "keywords":[],
    "author":"",
    "license": "ISC",
    "devDependencies":{// other module need to install
        "@babel/cli":"7.21.0",
        "@babel/core":"7.21.4",
    }
}
```

[官方文档](https://docs.npmjs.com/cli/v9/configuring-npm/package-json)

Q: what is the defference between dependencies and devdependencies?  
devDependencies  里面的插件只用于开发环境，不用于生产环境，而 dependencies  是需要发布到生产环境的。
比如我们写一个项目要依赖于jQuery，没有这个包的依赖运行就会报错，这时候就把这个依赖写入dependencies ；
而我们使用的一些构建工具比如glup、webpack这些只是在开发中使用的包，上线以后就和他们没关系了，所以将它写入devDependencies。

[webpack解析文档](https://zhaomenghuan.js.org/blog/webpack-introduction.html)
