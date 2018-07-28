# 基础

## 变量

### 声明

| 方式 | 作用域 | 重复声明 | 声明提升 | 暂时性死区 | 挂载全局对象 | 说明 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| var | 函数作用域 | √ | √ | × | √ | |
| let | 块级作用域 | × | × | √ | × | |
| const | 块级作用域 | × | × | √ | × | 声明必须赋值，不可改变。语义：指针不变。 |

说明：

- 声明提升(hoisting)：变量和函数的声明在编译阶段初始化内存空间。
- 暂时性死区(TDZ)：声明语句前访问变量将抛出异常`ReferenceError`，这将导致`typeof`不安全。

### 作用域

### 类型

js中的变量类型分为基础类型和引用类型。

基础类型包含六种，`undefined`, `null`, `number`, `string`, `boolean`, `symbol`'。

引用类型即为对象。

#### 类型判断

基础类型使用`typeof`判断，其中`null`和函数返回值特殊。

内置类型使用`Object.prototype.toString()`判断。

对象类型使用`instanceof`判断。

```js
// typeof
typeof undefined;       // 'undefined'
typeof null;            // 'object'
typeof 1;               // 'number'
typeof true;            // 'boolean'
typeof 'demo';          // 'string'
typeof (() => null);    // 'function'
typeof {};              // 'object'

// 内置类型
Object.prototype.toString.call([]);     // '[object Array]'

// 对象类型
{} instanceof Object;   // true
```

## 运算符

## 语句