# 基础

## 生命组件

- React.createElement
- 函数组件
- 类组件

## 生命周期

- 装载
    - constructor：初始化state。
    - ~~~componentWillMount~~~
    - static getDerivedStateFromProps(prevProps, prevState)：返回新state。
    - render()：渲染DOM。
    - componentDidMount：挂载DOM后调用，在这里请求数据、添加事件监听。

- 更新
    - ~~~componentWillReceiveProps~~~
    - static getDerivedStateFromProps(prevProps, prevState)：返回新state。
    - shouldComponentUpdate(nextProps, nextState)：判断是否是要重新渲染
    - ~~~componentWillUpdate~~~
    - getSnapshotBeforeUpdate(prevProps, prevState)：async render获取之前的组件状态
    - render()：渲染
    - componentDidUpdate：更新完成

- 卸载
    - componentWillUnmount：卸载前调用

## 高阶组件

## PureComponent

浅对比更新组件