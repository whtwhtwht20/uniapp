<template>
	<view>
		<view>message</view>
		<button type="primary" @click="chooseImg">chooseImg</button>
		<!--  #ifdef H5 -->
		<view>h5才看得见</view>
		<!--  #endif -->
		<view v-for="item in imgArr">
			<image :src="item" style="width: 100%;" @click="previewImage(item)"></image>
		</view>
		
	</view>
	
</template>

<script>
	export default {
		data() {
			return {
				imgArr: []
			}
		},
		methods: {
			chooseImg() {
				uni.chooseImage({
					count:5,
					success:(res) => {
						this.imgArr = res.tempFilePaths;
					}
				})
			},
			previewImage(current) {
				uni.previewImage({
					current,
					urls: this.imgArr,
					loop: true,
					indicator:'number'
				})
			}
		}
	}
</script>

<style>
</style>
