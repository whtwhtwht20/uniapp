<template>
	<view>
		<view>导航跳转的学习</view>
		<navigator url="/pages/detail/detail?id=80">detail</navigator>
		<navigator url="/pages/message/message" open-type="switchTab">message</navigator>
		<button @click="goDetail">goDetail</button>
		<button @click="goMessage">goMessage</button>
	</view>
</template>

<script>
	export default {
		methods: {
			goDetail() {
				uni.navigateTo({
					url:'/pages/detail/detail?id=80'
				})
			},
			goMessage() {
				uni.reLaunch({
					url:'/pages/message/message'
				})
			}
		}
	}
</script>

<style>
</style>
