<template>
	<view>
		<view>list</view>
		<button @click="getUrl">getUrl</button>
		<button type="primary" @click="getStorge">getStorge</button>
		<view style="height: 200px; line-height: 200px;" v-for="item in list">{{item}}</view>
		<button @click="pullfresh">PullDownRefresh</button>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ['1','2', '3','4']
			}
		},
		onPullDownRefresh() {
			console.log('onPullDownRefresh');
			this.list = ['4','3', '2','1'];
			setTimeout(function () {
				uni.stopPullDownRefresh()
			}, 1000);
		},
		onReachBottom() {
			console.log('onReachBottom')
			this.list = this.list.concat(this.list);
		},
		methods: {
			pullfresh() {
				uni.startPullDownRefresh()
			},
			getUrl() {
				uni.request({
					url:'',
					success(res) {
						
					}
				})
			},
			getStorge() {
				uni.setStorage({
					key: 'id',
					data: 80,
					success() {
						console.log('success')
					}
				})
			}
		}
	}
</script>

<style>
</style>
