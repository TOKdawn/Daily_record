---
title: chart
date: 2018-03-28 17:42:04
tags: JavaScript
---

别跟我说啥echarts文档好,Chart就翻译了个目录,
Chart配色好看我就有Chart,
颜值高了不起啊!
抱歉,颜值高就是了不起...
<!--more-->

Vue项目中使用chart

##先跑起来:


	"vue-chartjs ": "3.3.1"//添加入package.json
	项目文件里新建一个.js文件
	import { Line } from 'vue-chartjs'//引入一个Chart对像
	
	export default { //模块化返回对象
    extends: Line, //继承自Line
    mounted() {
        this.renderChart({ //核心函数.两个参数,一个是数据,一个是参数
            labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
            datasets: [{
                label: 'Data One',
                backgroundColor: 'rgba(242,113,115,.4)',
                data: [40, 39, 10, 40, 39, 80, 40]
            }, {
                label: 'Data Two',
                backgroundColor: 'rgba(54,162,235,.4)',
                data: [60, 55, 32, 10, 2, 12, 53]
            }]
        }, { responsive: false, maintainAspectRatio: false })

     }
	}
	然后在一个vue文件中引入这个js,按组件的方式插入到页面即可
	<template>
      <LineExample></LineExample>
	</template>
	<script>
	   import LineExample from './chart.js'
	    export default {
	      components: {
	        LineExample
	      }
	    }
	</script>
	<style scoped>
	
	</style>
	
	
核心思想:引入Chart.js里的一种类型,然后创建一个对象继承它,并且设置数据和参数,最后把这个对象按组件的方式插入到vue中
	
##加点料


