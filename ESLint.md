## ESLint
### 1. 对象字面量
##### 对象字面量是定义对象的一种简要形式，目的在于创建包含大量属性的对象的过程。
##### 例如：
##### 创建一个普通对象
```javascript
var person = new Object()
```
##### 创建一个字面量对象
```javascript
var person = {
	name: "Alice",
	age: 22
}
```

### 2. ESLint rules
##### 0 — 不验证 
##### 1 — 警告 
##### 2 — 错误 

### 3. ESLint rules website
#### http://eslint.cn/docs/rules/


### 4. 具体的规则（常用型）
(1) react/boolean-prop-naming: Enforces consistent naming for boolean props 
布尔属性的命名一致性 需要以is或has为前缀
<br>
(2) react/display-name: Prevent missing displayName in a React component definition 
组件定义时需要定义组件名称
<br>
(3) react/no-danger: Prevent usage of dangerous JSX properties 
禁止使用危险的JSX属性
<br>
(4) react/no-deprecated: Prevent usage of deprecated methods, including component lifecyle methods 
禁止使用过时的方法，包括组件生命周期方法
<br>
(5) react/no-did-mount-set-state: Prevent usage of setState in componentDidMount 
禁止在 componentDidMount方法中使用setState
<br>
(6) react/no-did-update-set-state: Prevent usage of setState in componentDidUpdate 
禁止在componentDidUpdate使用setState
<br>
(7) react/no-typos: Prevent common casing typos
确保没有声明静态类属性和生命周期方法的大小写错误
<br>
(8) react/no-unescaped-entities: Prevent invalid characters from appearing in markup 
防止标签中出现无效字符
<br>
(9) react/no-unknown-property: Prevent usage of unknown DOM property (fixable) 
禁止使用未知的DOM属性
<br>
(10) react/react-in-jsx-scope: Prevent missing React when using JSX 
防止在使用JSX时丢失React
<br>
(11) react/self-closing-comp: Prevent extra closing tags for components without children
防止没有孩子的组件有额外的闭标签
<br>
(12) react/jsx-closing-bracket-location: Validate closing bracket location in JSX
验证JSX中闭括号的位置
<br>
(13) react/jsx-closing-tag-location: Validate closing tag location in JSX
验证JSX中闭标签的位置
<br>
(14) react/jsx-curly-spacing: Enforce or disallow spaces inside of curly braces in JSX attributes and expressions
花括弧内两边是否留空格
<br>
(15) react/jsx-equals-spacing: Enforce or disallow spaces around equal signs in JSX attributes
等号两边是否留空格
<br>
(16) react/jsx-indent-props: Validate props indentation in JSX 
验证属性缩进
例如
```javascript
"react/jsx-indent-props": [2, 4]
```
<br>
(17) react/jsx-space-before-closing: Validate spacing before closing bracket in JSX
验证闭标签前面的空格
<br>
(18) react/jsx-tag-spacing: Validate whitespace in and around the JSX opening and closing brackets
验证标签周围的空格
<br>
(19) ***react/jsx-uses-react: Prevent React to be incorrectly marked as unused***
***防止React被错误的标记为未使用***
<br>
(20) react/react-in-jsx-scope: Prevent missing React when using JSX 
防止在使用JSX的时候丢失react
reason: When using JSX, ```<a/>``` expands to ```React.createElement("a")```. Therefore the React variable must be in scope.
<br>
(21) arrow-parens: Require parens in arrow function arguments
箭头函数变量需要括号
例如
```javascript
a => {}    //bad
(a) => {}  //good
```


