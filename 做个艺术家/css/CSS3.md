#CSS3
	
__追加的属性选择器:__
	
	[id*=fish]//所有ID中包含fish的节点
	[id^=fish]//所有ID以fish开始的节点
	[id$=fish]//所有ID以fish结束的节点
__类选择器__
	
	p.left//p标签下class为left的节点
__伪类选择器__
	
	a:link//未被访问的连接
	a:visited//已经被访问的连接
	a:hover//指针移动到上面的连接
	a:active//正在被点击的连接
	a:focus//获得光标聚焦的连接
	p:first-line//节点里的第一行文字
	p:first-letter//节点里的第一个文字
	p:before//在某个节点之前插入
	p:after//在某个节点之后插入
	:root//当然页面的根节点
	body *:not(h1)//对body进行样式设置但是不应用于body下的h1
	:empty//节点下为空时的样式
	:target//通过连接跳转过去的当前活动节点的样式
	:first-child//第一个子节点
	:last-child//最后一个子节点
	:nth-child(n)//第n个子节点
	:nth-child(odd)//单数个子节点,但是又问题,这个单数是真的于所有节点.不论什么类型节点
	:nth-child(even)//偶数个子节点
	:nth-of-type(odd)//这样就可以只针对谋类型的节点取单双数
	:nth-child(4n+1)//4个子节点为一组,设置这组中的第一个样式
	:only-child//只对有一个子节点的元素设置样式
__UI伪静态选择器__

	:enable//元素可用时的样式
	:disabled//元素不可以时的样式.
	:read-only//选择器被用来指定当元素处于只读状态时的样式.
	:read-write//非只读时的样式
	:cheacked//当表单中的单选框或者复选框时处于被选取时的样式
	:default//选择器被打开时默认处于选中状态下的项的样式
  	:indeterminate//一组单选框中没有任何一个选项设定为选中状态时
	:selection//处于被选定状态的元素
	:invalid//类型不正确时的样式比如邮箱地址
	:valid//类型正确时的样式
	:in-range//数据在一定区间内时的样式
	:out-of-range//超出一定区间时的样式
	div~p{}//div的兄弟元素(为p的兄弟元素)的样式