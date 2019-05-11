## dva 目录结构
src/assets 静态文件
src/components 组件
src/models 数据  reducer  saga state  
src/routes 路由
src/services 数据请求
src/utils 工具

## dva
Model
State  表示Model的状态数据 通常表现为一个javascript对象，操作的时候每次都要当作immutable对象 保证每次都是全新对象 没有引用关系
Action
Action是一个普通的js对象 他是改变state的唯一途径 无论从UI事件 网络回调 还是WebSocket等数据源获取的数据 最终都会通过dispatch方法 调用一个action从而改变对应的数据 需要注意的是 dispatch是在组件connect Models以后 通过props传入的、

## Redux 数据层框架
