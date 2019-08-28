<template>
	<view >
			
		<!-- <view class="d-flex bg-white border-top position-fixed bottom-0 left-0 right-0" style="height: 90upx;">
			<view class="flex-1 d-flex j-center a-center flex-column line-h">
				<view class="iconfont icon-xihuan line-h"></view>
				收藏
			</view>
			<view class="flex-1 d-flex j-center a-center flex-column line-h">
				<view class="iconfont icon-gouwuche line-h"></view>
				购物车
			</view>
			<view style="flex: 2.5;" class="text-white main-bg-color d-flex j-center a-center" hover-class="main-bg-hover-color">加入购物车</view>
		</view> -->
		
		<!-- <view style="display: inline-block; background: #007AFF; width: 187.5upx; height: 150upx;"></view>
		<view style="display: inline-block; background: #09BB07; width: 187.5upx; height: 150upx;"></view>
		<view style="display: inline-block; background: #6D6D72; width: 375upx; height: 150upx;"></view> -->
		
		<!-- <view style="line-height: 1; display: inline-block; background: #007AFF; width: 371upx; height: 150upx; border-right: 4upx solid red;"></view>
		<view style="line-height: 1; display: inline-block; background: #09BB07; width: 375upx; height: 150upx;"></view> -->
		
		<scroll-view scroll-x="" class="scroll-row">
			<view style="width: 200upx; background: #007AFF;" class="border scroll-row-item">1</view>
			<view style="width: 200upx; background: #007AFF;" class="border scroll-row-item">2</view>
			<view style="width: 200upx; background: #007AFF;" class="border scroll-row-item">3</view>
			<view style="width: 200upx; background: #007AFF;" class="border scroll-row-item">4</view>
			<view style="width: 200upx; background: #007AFF;" class="border scroll-row-item">5</view>
		</scroll-view>
		<view class="line-through">aini 爱你</view>
		
		<view class="row p-2">
			<view class="span-4 text-center py-2">
				<view class="iconfont icon-VIP"></view>
				1
			</view>
			<view class="span-4 text-center py-2">
				<view class="iconfont icon-VIP"></view>
				2
			</view>
			<view class="span-4 text-center py-2">
				<view class="iconfont icon-VIP"></view>
				3
			</view>
			<view class="span-4 text-center py-2">
				<view class="iconfont icon-VIP"></view>
				4
			</view>
			<view class="span-4 text-center py-2">
				<view class="iconfont icon-VIP"></view>
				5
			</view>
			
			<view class="span-4 text-center">1</view>
			<view class="span-4 text-center">2</view>
			<view class="span-4 text-center">3</view>
			<view class="span-4 text-center">4</view>
			<view class="span-4 text-center">5</view>
			<view class="span-4 text-center">1</view>
			<view class="span-4 text-center">2</view>
			<view class="span-4 text-center">3</view>
			<view class="span-4 text-center">4</view>
			<view class="span-4 text-center">5</view>
		</view>
		
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				show: false,
				title: '221Hello'
			}
		},
		onLoad() {
			

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50upx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
