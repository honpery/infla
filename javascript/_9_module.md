# 模块化

## script

## CommonJS

同步加载

主要实现：node.js

```js
// 导出模块 a.js
module.exports = () => null;
exports.name = 'a module';

// 导入模块 main.js
const a = require('a.js');
```

## AMD

异步加载，依赖前置

主要实现：require.js

```js
// 导出模块 a.js
define([], () => {})
```

## CMD

异步加载，按需加载

主要实现：sea.js

```js
// 定义模块 a.js
define(function (require, exports, module) {
});
```

## ES6 module

编译阶段分析依赖，静态处理。

```js
// 导入
import a from 'a.js';

// 导出
export const name = 'a module';
export default () => null;
```