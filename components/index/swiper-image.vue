<template>
	<view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" circular>
			<block v-for="(item, index) in resdata" :key="index">
				<swiper-item>
					<view class="swiper-item" @tap="event(item)">
						<image :src="item.src"
						lazy-load
						style="height: 350upx;"></image>
					</view>
				</swiper-item>
			</block>
			
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		props: {
			resdata: Array
		},
		methods: {
			event(item) {
				console.log('点击了轮播图')
			}
		}
	}
</script>

<style>

</style>
