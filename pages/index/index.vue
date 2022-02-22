<template>
	<view class="content">
		<!-- <image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view> -->
		<test/>
	</view>
</template>

<script>
	import test from '../../components/demo.vue'
	export default {
		components: {
			test,
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad(option) {
			console.log('onLoad', option)
		},
		onHide(option) {
			console.log('onHide', option)
		},
		onReady(option) {
			console.log('onReady', option)
		},
		onShow(option) {
			console.log('onShow', option)
		},
		onUnload(option) {
			console.log('onUnload', option)
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
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
