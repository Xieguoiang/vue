<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>one</title>
</head>
<body>


	<div id="box">
	 <!-- 声明式渲染 {{xxx}}-->

	 <!-- v-text 纯文本渲染 -->

	 <!-- v-html 标签式渲染 -->
	 
	 <!-- v-model   数据双向绑定  多于与input啊 表单啊等等 -->

	 <!-- v-bind指令  用于绑定html特性 比方说属性  id 啊  class等等,Mustache 语法不能作用在 HTML 特性 -->

	 <!-- v-show 和 v-if都是控制元素的显示隐藏 值为false那么隐藏 / 值为true则为true-->
     <!-- v-show 控制display的属性 来控制显示隐藏 
	 v-if是控制dom的是否渲染来控制显示隐藏 -->

	<!--   和v-if配合的有v-else
	  当v-if显示 那么v-else隐藏 如果v-if元素隐藏 那么v-else显示 -->

		<p>
			{{msg}}    <!--  不会随数据变化而变化 -->
		</p>
		<p v-text="msg"></p>
		<p v-html="msg"></p>
		<input type="text" v-model="msg"> <br>
		<input type="text" v-model="one"> <input type="text" v-model="Symbol"> 
		<input type="text" v-model="two">
		<button @click="getSum">求和</button> <!--  @click 是 v-on-click的缩写 -->



		<div :id="val"></div>    <!-- v-bind:id= "val" 的缩写 -->
		<div v-show="isShow">走进vue这个坑</div>
		<div v-if="isShow">走进vue这个坑222222</div>
		<div v-else>我是和v-if配合使用的v-else</div>

		<!-- 问题 -->
		<!--  -->
		<!--  -->
		<input type="text">    文本框1
		<input type="text">    文本框2

		<input type="text">    文本框3

		<button>判断</button>

		<p>俩者长度相等</p>
		<p>俩者完全相等</p>
		<p>俩者不相等</p>
		<p>俩者不完全相等</p>   <!-- 这个拓展 -->
	

	</div>






	<script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.5.16/vue.min.js"></script>	
	<script>
		new Vue({    // 新建一个实例
          el: '#box',    //  根元素是 id 为 box的盒子
          data: {    // 存放数据的
          	msg:'你好',
          	one:'',
          	two:'',
          	Symbol:'',
          	val:'ids',
          	isShow:false

          },
          methods: {    // 定义方法的
            	
          	getSum(){        // parseInt() 字符串转换为数字
          		if(this.Symbol == '+'){
					alert(parseInt(this.one) + parseInt(this.two))
          		}
          		if(this.Symbol == '-'){
					alert(parseInt(this.one) - parseInt(this.two))
          		}
          		if(this.Symbol == '*'){
					alert(parseInt(this.one) * parseInt(this.two))
          		}
          		if(this.Symbol == '/'){
					alert(parseInt(this.one) / parseInt(this.two))
          		}
          	}


          }


        })

	</script>
</body>
</html>
