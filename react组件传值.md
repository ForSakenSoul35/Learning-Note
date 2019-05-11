# react组件传值
## 父组件向子组件传值 props
```
//父组件
class Father extends Component{
  constructor(props){
    super(props);
    this.state ={
      checked:true
    }
  }
  render(){
    return (
      <ToggleButton text = "Toggle me" checked ={this.state.checked }/>
      //向组件传递 两个值 
    )
  }
}
//子组件
class ToggleButton extends Component{
  render(){
   <label>
        {this.props.text}<input type="checkbox" checkd= {this.props.checked}/>
   </label>
  }
}
```

## 子组件向父组件传值
## 兄弟组件传值