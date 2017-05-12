#canvas
	<script>
	function draw(id){
	//body加载完成调用draw这个自定义函数并且把canvas标签的id传入
	var canvasQVQ = docment.getElementById(id);//获取id对应的canvas
	var context = canvasQVQ.getContext('2d');//以2d形式开始绘制
	}
	</script>
	<body onload="draw('画布id');">//绘制canvas
	<canvas id="画布id" width="500" height="350"></canvas>
	</body>
	常用方法
	context.fillStyle填充风格主要是颜色
	context.fillRect(0,0,150,75)填充的位置前两位是坐标,后两位是长度和宽
	context.moveTo(110,0);光标移动到指定坐标
	context.lineTo(110,100);连线到某坐标
	context.stroke();对已经设定的移动轨迹进行绘制
	context.strokeStule();绘制风格
	ctx.beginPath();开始或者说重置路径画笔
	ctx.font();设置字体风格
	fillText(text,x,y) - 在 canvas 上绘制实心的文本
	strokeText(text,x,y) - 在 canvas 上绘制空心的文本