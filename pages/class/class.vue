<template>
	<view>
		<view style="display: flex;justify-content: center;font-size: 100upx;">
			{{text}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				text: "2342"
			}
		},
		onLoad() {
			console.log(getApp().globalData.text)
			console.log(uni.getStorageSync('index'))
			uni.$on('index', e => {
				console.log('分类页')
				// console.log(e)
				this.text = e.data
			})
		},
		onShow() {
			this.text = getApp().globalData.text
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
