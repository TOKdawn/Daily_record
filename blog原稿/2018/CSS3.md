# CSS3
虽然现在前端技能树愈加的复杂繁琐,但是CSS还是不得不学的东西
<!—more—>

## LESS/SCSS
* 计算属性
* 样式变量
* 混合
* 嵌套

## 伪元素与伪类
单冒号:用于 CSS3 伪类，双冒号::用于 CSS3 伪元素。对于 CSS2 中已经有的伪元素，例如 :before，单冒号和双冒号的写法 ::before 作用是一样的。

* :focus 聚焦伪类(当前页面活的焦点的元素)
* ::selection 选定伪元素(被鼠标点击拖动框出来的元素)


### 伪元素实例

浮动清除:

```
.clear:after {
    content: '';
    display: block;
    clear: both;
}
```

画分割线:

```
  .spliter::before, .spliter::after {
      content: '';
      display: inline-block;
      border-top: 1px solid black;
      width: 200px;
      margin: 5px;
    }
```

## 属性选择符
标签名[属性名]
p.s.

```
		img[title]  //带有title属性的img标签
		a[href^="http://"] //http连接
		a[href^="https://"] //https连接
		a[href~="www"] //含有www的连接
		
```

## 子代选择器
* 空格 寻找所有小辈
* > 寻找直系子代
* + 寻找同辈



要选择的子元素:nth-child(在父级元素的位置)   //所有父元素下的子节点都参与计数
p.s.
`tr:nth-child(odd)//所有奇数的tr`

父级元素  要选择的子元素类型:nth-of-type(在父级元素的位置)   //只有对应类型的子节点参与计数

p.s.
`body p:nth-child(3)//body内的第3个p`

位置计数从1开始,odd为奇数,even为偶数,某数n (P.S.  3n)选取为所有某数 (P.S. 3)倍数的元素 ,之后再 + 某数为从第某数算起

p.s.
`tr:nth-child(3n+4) //从第四个元素算起三的倍数`

### target选择器
众所周知,我们可以通过给a标签设置 # id的形式让页面进行跳转(页面跳转时# id会添加到当前url的最后).:target标签针对的就是id,用于获取当前正在被跳转的id(即此时出现在url内的id)可以通过为# id 和# id:target 设置不同的css样式做到很多很酷炫的事情

### :not()选择符
区反选择符,括号内添加要取反的规则()

### :empty
没有子元素的元素

### input所属

* :enabled 所有启用的
* :disabled 所有禁用的
* : checked 单个被选中的

### a所属

* :link 未被访问的
* :visited 访问过的
* :active 点击状态的



