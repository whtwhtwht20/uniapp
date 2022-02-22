<template>
	<view>
		<view>
			<text>唱歌篮球打篮球</text>
		</view>
		<!-- <view>
			<text selectable>唱歌篮球打篮球</text>
		</view>
		<view>
			<text space="emsp">唱歌  篮球打篮球</text>
		</view>
		<view>
			<text space="ensp">唱歌  篮球打篮球</text>
		</view>
		<view>
			<text decode>&ensp;</text>
		</view> -->
		<view class="blue" hover-class= "pink">
			<view class="red" :hover-start-time="3000" :hover-stay-time="3000"  hover-class= "yellow" hover-stop-propagation>
				big Box
			</view>
		</view>
		<button disabled>按钮</button>
		<button loading size="mini">按钮mini</button>
		
		<button type="primary" plain>按钮</button>
		<image src="../../static/logo.png" mode="aspectFit"></image>
		<image src="../../static/logo.png" mode="aspectFill"></image>
	</view>
</template>

<script>
	export default {
		onLoad(option) {
			console.log(option)
		}
	}
</script>

<style>
	.red {
		width: 100px;
		height: 100px;
		background: red;
	}
	.blue {
		width: 200px;
		height: 200px;
		background: blue;
	}
		
	.pink {
		background: pink;
	}
	.yellow {
		background: yellow;
	}
	
</style>
