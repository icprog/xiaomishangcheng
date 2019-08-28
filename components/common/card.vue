<template>
	<view class="card">
		<!-- head -->
		<view v-if="showhead" class=" p-2 border-bottom main-border-color">
			<slot name="title">
				<text v-if="headTitle" class="font-md font-weight">{{headTitle}}</text>
			</slot>
		</view>
		<!-- body -->
		<view>
			<image v-if="bodyCover" :src="bodyCover" mode="widthFix"></image>
			<slot></slot>
			<!-- <slot name="title">
				<text class="font-md font-weight">123</text>
			</slot> -->
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			// 封装标题
			headTitle: String,
			// 封装图片
			bodyCover: String,
			// 是否显示头部
			showhead: {
				type: Boolean,
				default: true
			}
		}
	}
	
</script>

<style>
</style>
