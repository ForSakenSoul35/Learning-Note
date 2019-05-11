# redux-saga
1. 是一个用于管理redux应用异步操作的中间件（异步action） redux-saga 通过创建  Sagas 将所有的异步操作逻辑收集到一个地方集中处理 可以用来替代redux-thunk中间件
应用的逻辑
Reducer负责处理action的state的更新
Sagas负责协调那些复杂或异步的操作
Sagas是通过Generator函数来创建的 