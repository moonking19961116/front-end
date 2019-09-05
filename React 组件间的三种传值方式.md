## React 组件间的传值

难度由易到难为 父组件向子组件传值， 子组件向父组件传值， 兄弟组件间传值

#### 1. 父组件向子组件传值（通过props）

##### 父组件：

```javascript
export class Father extends Component{
    constructor(props){
        super(props)
        this.state = {name: 'moon'}
    }
    
    render() {
        return(
        	<Child name={this.state.name}>
        )
    }
}
```

##### 子组件：

```javascript
export class Child extends Component{
    constructor(props){
        super(props)
        this.state = {}
    }
    
    render(){
        return(
        	<div>The name of the user: {this.props.name}</div>
        )
    }
}
```



#### 2. 子组件向父组件传值（回调函数）

##### 父组件：

```javascript
export class Father extends Component{
    constructor(props){
        super(props)
        this.state = { name: '' }
    }
    
    modifyName = (newName) => {
        this.setState(
        	{ name: newName }
        )
    }
    
    render() {
        return(
        	<Child changeName={this.modifyName}>
        )
    }
}
```

##### 子组件：

```javascript
export class Child extends Component{
    constructor(props){
        super(props)
        this.state = { fatherName: 'father' }
    }
    
    handleClick = (name) => {
        this.setState(
        	{ fatherName: name }
        )
        this.props.changeName(name)  //执行父组件中的changeName并传参
    }
    
    render(){
        return(
        	<div onClick={this.handleClick.bind(this, 'anotherName')}>
            	<p>{this.state.fatherName}</p>
            </div>
        )
    }
}
```



#### 3. 兄弟组件间的传值

* 先由子组件B向父组件A传值
* 再由父组件A将这个值传给其另一个子组件C
