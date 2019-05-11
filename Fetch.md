## 发送请求

从远程地址中获取数据或资源
fetch('https://mywebsite.com/mydata.json')
fetch还有可选的第二个参数，用来定制HTTP请求的一些参数，可以指定header参数 或者指定使用POST方法
```
fetch('https://mywebsite.com/mydata.json',{
  method:'POST',
  headers:{
    'Accept':'application/json',
    'Content-type':'application/json',
  },
  body:JSON.stringify({
    firstParm:'yourValue',
    secondParn:'yourOtherValue'
  })
})
```
## 处理数据
网络请求 天然就是一种异步操作  Fetch方法会返回一个Promise，这种模式可以简化异步风格的代码
```
  getMoviesFromApiAsync(){
    return fetch("'https://facebook.github.io/react-native/movies.json'")
    .then((response)=>response.json())
    then((responseJson)=>{
      return responseJson.movie
    })
  }
```                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         