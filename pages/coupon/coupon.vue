<template>
	<view class="container">
		<view class="cont1">
			<view class="cont1-a">
				<text>全部</text>
			</view>
			<view class="cont1-b">
				<text style="">未使用</text>
			</view>
			<view class="cont1-a">
				<text>已使用</text>
			</view>
		</view>
		<view class="cont2" style="background-image: url(../../static/WechatIMG423.png);width: 300upx;height: 254upx;">
			
		</view>
		
		
		
		<view class="demo_div">
			<homePage></homePage>
		</view>
	</view>
</template>

<script>
	import homePage from "../../components/homepage/homepage.vue";
	export default {
		data() {
			return {
				
			}
		},
		components: {
		            homePage
		        },
		methods: {
				
		}
	}
</script>

<style>
	.container{
		width: 90%;
		border: #0000FF 1px solid;
		margin: 15upx auto;
		
	}
	.demo_div {
		left: 0;
		position: fixed; 
		bottom: 0; 
		width: 100%; 
	    } 
	.cont1{
		display: flex;
		justify-content: space-around;
		width: 100%;
		height: 84upx;
		border-radius: 20upx;
		background-color: #FFFFFF;
	}
	.cont1-a{
		width: 33.3%;
		height: 100%;
		text-align: center;
		line-height: 84upx;
		font-size: 36upx;
	}
	.cont1-b{
		width: 33.3%;
		height: 80%;
		margin-top: 8.4upx;
		line-height: 67.2upx;
		text-align: center;
		border-left: #E4E4E4 1px solid;
		border-right: #E4E4E4 1px solid;
		font-size: 36upx;
	}
</style>
