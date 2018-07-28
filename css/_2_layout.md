# 布局

## BFC：块级格式化上下文(block format context)

触发条件：

- float: left, right
- position: absolute, fixed
- overflow: hidden, auto, scroll
- display: inline-block, table-cell, table-caption

## 盒模型：display

## 浮动：float

## 定位：position

### position属性值

| 属性值 | 名称 | 脱离文档流 | 基准点 | 说明 |
|:----:|:----:|:----:|:----:|:----:|
| static | 正常定位 | × | 无 | 默认值，忽略top/left/right/bottom/z-index属性 |
| relative | 相对定位 | × | 自身位置 | |
| absolute | 绝对定位 | √ | 最近非static父节点 | 转为行内元素 |
| fixed | 固定定位 | √ | 视窗 | |
| sticky | 粘性布局 | × | 最近非static父节点 | |

### z-index

z-index只对定位元素有效，其取值可以为：z-index: auto | [number] | inherit;

层叠上下文(stacking context)：`z-index`设置除了`auto`外的值后会创建新的层叠上下文。

同一上下文层叠次序(stacking order)：

- 背景边框
- 负z-index值
- 块级盒
- 浮动盒
- 行内盒
- z-index为0
- 正z-index值

不同上下文后来者排在前面。

css3新增属性对层叠上下文影响：
[TODO]

[参考](https://webdesign.tutsplus.com/zh-hans/articles/what-you-may-not-know-about-the-z-index-property--webdesign-16892)

## 弹性盒布局：flex

- display
    - flex
    - inline-flex
- align-items
- justify-content


## 网格布局：Grid
