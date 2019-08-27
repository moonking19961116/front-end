## CSS flex灵活布局的使用

#### 1.父盒子模型下的子盒子模型全部灵活布局

**例如：**

**html:**

```html
<div class='bottom'>
    <div class='button'></div>
    <div class='button'></div>
    <div class='button'></div>
</div>
```

**CSS:**

```CSS
.bottom{
	width: 100%;
	display: flex;
}
```


	.button{
		flex: 1;   //所有的button平分这个bottom
	}


#### 2. 父盒子模型下一个子盒子定宽，其余使用flex

**html:**

```html
<div class='bottom'>
    <div class='button1'></div>
    <div class='button'></div>
    <div class='button'></div>
</div>
```

**CSS:**

```css
.bottom{
	width: 100%;
	display: flex;
}
```

```css
.button1{
    width: 10rem;
}
.button{
    flex: 1;  //此时总宽度会先减去定宽盒子的宽度，剩下的宽度由剩下的子盒子平分
}
```

**//flex还有一个注意的点：**

```css
flex-direction: row或col;
```













