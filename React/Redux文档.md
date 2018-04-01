# Redux



## 基础

### Action

**Action** 是把数据从应用传到 store 的有效载荷。它是 store 数据的**唯一**来源。

**Action 创建函数** 就是生成 action 的方法。



### Reducer

**Reducers** 指定了应用状态的变化如何响应 [actions](http://www.redux.org.cn/docs/basics/Actions.html) 并发送到 store。



### Store

Store 有以下职责：

- 维持应用的 state；
- 提供 [`getState()`](http://www.redux.org.cn/docs/api/Store.html#getState) 方法获取 state；
- 提供 [`dispatch(action)`](http://www.redux.org.cn/docs/api/Store.html#dispatch) 方法更新 state；
- 通过 [`subscribe(listener)`](http://www.redux.org.cn/docs/api/Store.html#subscribe) 注册监听器;
- 通过 [`subscribe(listener)`](http://www.redux.org.cn/docs/api/Store.html#subscribe) 返回的函数注销监听器。



### 数据流

**严格的单向数据流**是 Redux 架构的设计核心。

Redux 应用中数据的生命周期遵循下面 4 个步骤：

1. **调用** [`store.dispatch(action)`](http://www.redux.org.cn/docs/api/Store.html#dispatch)。
2. **Redux store 调用传入的 reducer 函数。**
3. **根 reducer 应该把多个子 reducer 输出合并成一个单一的 state 树。**
4. **Redux store 保存了根 reducer 返回的完整 state 树。**





## 高级

### 异步Action

###### 一般情况下，每个 API 请求都需要 dispatch 至少三种 action：

- **一种通知 reducer 请求开始的 action。**
- **一种通知 reducer 请求成功的 action。**
- **一种通知 reducer 请求失败的 action。**



###### 处理异步 action 的方式

- [redux-thunk](http://github.com/gaearon/redux-thunk) — 用最简单的方式搭建异步 action 构造器
- [redux-promise](https://github.com/acdlite/redux-promise) 或者 [redux-promise-middleware](https://github.com/pburtchaell/redux-promise-middleware) 来 dispatch Promise 来替代函数。
- 使用 [redux-observable](https://github.com/redux-observable/redux-observable) 来 dispatch Observable。
- 使用 [redux-saga](https://github.com/yelouafi/redux-saga/) 中间件来创建更加复杂的异步 action。
- 使用 [redux-pack](https://github.com/lelandrichardson/redux-pack) 中间件 dispatch 基于 Promise 的异步 Action。
- 写一个自定义的 middleware 来描述 API 请求，就像这个 [真实场景的案例](http://www.redux.org.cn/docs/introduction/Examples.html#real-world) 中的做法一样。



### Middleware

**提供的位于 action 被发起之后，到达 reducer 之前的扩展点。** 可以利用 Redux middleware 来进行日志记录、创建崩溃报告、调用异步接口或者路由等等。



## API文档

[createStore](http://www.redux.org.cn/docs/api/createStore.html)

[Store](http://www.redux.org.cn/docs/api/Store.html)

[combineReducers](http://www.redux.org.cn/docs/api/combineReducers.html)

[applyMiddleware](http://www.redux.org.cn/docs/api/applyMiddleware.html)

[bindActionCreators](http://www.redux.org.cn/docs/api/bindActionCreators.html)

[compose](http://www.redux.org.cn/docs/api/compose.html)

