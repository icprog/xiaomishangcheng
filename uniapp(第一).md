一.	在 App.vue中引入全局样式
		1 引入样式库
		  uni.css  // 官方UI库
			animate.css  // css动画库
			icon.css  // 图标库
			common.css  // 公共样式


二. 在common.css中设置全局样式 

三. 在page.json中进行全局配置--底部tabbar导航开发

四.		什么是UI基础库？
  .1 	颜色
				  背景颜色
					边框颜色
					文本颜色
	.2 	布局
	.3 	边框
	.4 	内边距
	.5	外边距
	.6	字体大小
	.7	行高
	.8	flex布局
	
五. nvue基础
	.(一) 组件使用注意事项
		--1、文字（最好）写在text中
		--2、<list>的子组件只能包括以下四种组件或是 fix 定位的组件
				<cell>: 用于定义列表中的子项列表项，类似于HTML中的ul 之于 li。 weex会对<cell>进行高效的内存回收以达到更好的性能
				<header>：实现吸顶效果！！ 当<header>到达屏幕顶部时，吸附在屏幕顶部
				<refresh>：用于给列表添加下拉刷新的功能
				<loading>：用法与特性和<refresh>类似，用于给列表添加上拉加载更多的功能 （下拉不建议用loadmore，多下拉几次会有bug）
		--3、图片要给指定宽高
	.(二) nvue中cssd 注意事项
			1. 单位只支持px, 不支持em,rem,pt,%,upx
			2. 宽度、高度问题： 宽：750px=100%, 高： 1250px=100%
			3. 默认为flex布局 (即它的父元素身上   div组件默认是： display：flex;felx-direction:column; flex-wrap: nowrap;)
			4. 不能合着写(eg: border: 1px solid red;--> border-width:1px;border-style:solid;border-color:red)
			5. 背景颜色只能用background-color
			6. 选择器只支持单类
			7. 引入要用<style src="@/common/nvue-common.css"></style>
	.(三) nvue和vue之间的通讯
			1. --在nvue中使用 uni.postMessage(data) 发送数据通讯，data为JSON格式（键值对的值仅支持string);
			   --在App.vue里使用 onUniNViewMessage 进行监听
				 
			2. --在vue中使用 plus.webview.postMessageToUniNView(data, nvueId) 发送消息， data为JSON 格式（键值对的值仅支持string），
					   nvueId为nvue所在webview的id，webview的id获取方式参考：$getAppWebview()
				 --在nvue里引用globalEvent 模块监听 plusMessage 事件	
			3. vue和nvue共享的变量和数据
				 --nvue不支持vuex
				 --方式一：uni.storage vue和nvue页面可以使用相同的uni.storage存储（这个存储是持久化的，比如登录状态可以保存在这里）
				 --方式二：globalData 小程序有globalData机制，这套机制在uni-app里也可以使用，全端通用。在App.vue文件里定义globalData，
									通过getApp().globalData获取数据
				 