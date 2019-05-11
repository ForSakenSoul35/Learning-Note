```
@connect(({login,loading})=>({
  login,
  submitting:loading.effects['login/login'],
}))
export default class LoginPage extends Component {
  ...
}
```
注解会自动在LoginPage组件外面包裹一层Connect组件,这个组件把redux状态树种我们需要的值传入LoginPage组件的props中
作用 就是对redux中的state加工 然后把声明的login传入子组件的Props