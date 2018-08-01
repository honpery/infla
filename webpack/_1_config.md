# 配置

## entry

> 入口起点

```js
{
    // 简写：entry: string | string[]
    entry: 'app.js',            // main.js
    entry: ['c1.js', 'c2.js'],  // main.js, 这里入口文件同时引用两个依赖

    // 对象：entry: {[name]: string | string[]}
    entry: {main: 'main.js', vendor: 'vendor.js'},   // main.js, vendor.js
    entry: {main: ['main.js', 'c2.js']},             // main.js，这里入口文件同时引用两个依赖
}

```

## output

> 输出

```js
{
    output: {
        // 输出目录，必填
        path: 'dist',

        // 输出文件名，必填，多入口可以使用占位符[name], [hash]
        filename: '[name].[hash:8].js',

        // 块文件名
        chunkname: '[name].[chunkhash:8].chunk.js',

        // 公共目录[TODO]
        publicPath: '',

        // 
        libraryTarget: "",
    }
}

```

## mode

> 零配置模式

```js
{
    mode: 'production' | 'development' | 'none',
}
```

1. development
2. production

## target

> 构建目标

## resolve

> 模块解析配置

```js
{
    resolve: {
        extensions: "",
        alias: "",
        modules: "",
        mainField: "",
        mainFiles: ""
    }
}
```

## module.rules

> loader用于对模块源码进行转换

1. `test`属性：应该被转换的文件。
2. `use`属性: 转换使用loader。

特性：

1. loader支持链式传递，执行顺序与声明顺序相反。

## plugins

> 插件用于解决loader无法实现的其他事
