<template>
	<view class="container">
		<view class="contents">
			<view class="cont1">
				<view class="cu-bar search bg-white">
					<view class="search-form round">
					  <text class="cuIcon-search"></text>
					  <input type="text" placeholder="搜索图片、文章、视频" confirm-type="search"></input>
					</view>
				</view>
				<view class="cont1-a">
					<image src="../../static/test1.png" mode="aspectFit"></image>
				</view>
				
				<view class="cont1-b"v-on:click="is_sortByName()">
					<text>推荐筛选</text>
					<div :class="triangle"></div>
				</view>
				<view class="cont1-c"></view>
			</view>
			<view class="cont2">
				<view class="cont2-a flex">
				  <view class="cont2-a-item1">
					  <image src="../../static/1.png" mode="aspectFill"></image>
				  </view>
				  <view class="cont2-b">
					  <view class="cont2-b-item1">
					  	<text>纯天然紫皮红薯</text>
					  </view>
					  <view class="cont2-b-item2">
					  	<rich-text :nodes="nodes"></rich-text>
					  </view>
					  <view class="cont2-b-item3">
					  	<text class="cont2-b1-item3">销量最高</text>
						<text class="cont2-b2-item3">48元/箱</text>
					  </view>
				  </view>
				</view>
				
				<view class="cont2-a flex">
				  <view class="cont2-a-item1">
					  <image src="../../static/1.png" mode="aspectFill"></image>
				  </view>
				  <view class="cont2-b">
					  <view class="cont2-b-item1">
					  	<text>纯天然紫皮红薯</text>
					  </view>
					  <view class="cont2-b-item2">
					  	<rich-text :nodes="nodes"></rich-text>
					  </view>
					  <view class="cont2-b-item3">
					  	<text class="cont2-b1-item3">销量最高</text>
						<text class="cont2-b2-item3">48元/箱</text>
					  </view>
				  </view>
				</view>
				
				<view class="cont2-a flex">
				  <view class="cont2-a-item1">
					  <image src="../../static/1.png" mode="aspectFill"></image>
				  </view>
				  <view class="cont2-b">
					  <view class="cont2-b-item1">
					  	<text>纯天然紫皮红薯</text>
					  </view>
					  <view class="cont2-b-item2">
					  	<rich-text :nodes="nodes"></rich-text>
					  </view>
					  <view class="cont2-b-item3">
					  	<text class="cont2-b1-item3">销量最高</text>
						<text class="cont2-b2-item3">48元/箱</text>
					  </view>
				  </view>
				</view>
				
			</view>
			
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
				triangle:"trianglex",
				nodes: [{
						name: 'div',
						attrs: {
							class: 'div-class',
							style: 'color: #999999;'
						},
						children: [{
							type: 'text',
							text: '番薯别称甘储、甘薯、朱薯、金薯、番茹、红山药、玉枕薯、山芋、地瓜、甜薯、红薯、红苕、白薯、阿鹅、萌番薯。一年生草本植物，地下部分具圆形、椭圆形或纺锤形的块根，茎平卧或上升，偶有缠绕，多分枝，叶片形状、颜色常因品种不同而异，通常为宽卵形，叶柄长短不一，聚伞花序腋生，蒴果卵形或扁圆形，种子1-4粒，通常2粒，无毛。'
						}]
						}],
			}
		},
		components: {
		            homePage
		        },
		methods: {
				is_sortByName(){
					this.flag=!this.flag
					if(this.triangle=="trianglex"){
						this.triangle="triangles"
					}else{
						this.triangle="trianglex"
					}
				},
		}
	}
</script>

<style>
	page {
	background-color: #ffffff;
	}
	.container {
		
	}
	.contents{
		width: 100%;
		margin: 0 auto;
	}
	.cont1-a{
		width: 95%;
		height: 270upx;
		margin: 0 auto;
	}
	.cont1-a image{
		width: 100%;
		height: 100%;
		border-radius: 30upx;
	}
	.cont1-b{
		margin:0 0 12upx 12upx;
	}
	.cont1-c{
		width: 100%;
		border: #E4E4E4 1upx solid;
		margin-bottom: 28upx;
	}
	.cont2{
		width: 93%;margin:0 auto;
	}
	.cont2-a{
		width: 100%;
		height: 232upx;
		justify-content: space-between;
		margin-bottom: 40upx;
	}
	.cont2-a-item1{
		width: 37%;
		height: 232upx;
	}
	.cont2-a-item1 image{
		width: 100%;
		height: 100%;
		border-radius: 30upx;
	}
	.cont2-b{
		width: 61%;
		height: 232upx;
	}
	.cont2-b-item1{
		width: 100%;
		height: 50upx;
	}
	.cont2-b-item1 text{
		font-size: 32upx;
		font-weight: 700;
	}
	.cont2-b-item2{
		width: 100%;height: 114upx;margin:9upx 0 ;
	}
	.cont2-b-item2 rich-text{
		font-size: 16upx;
		display: -webkit-box;
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 5;
		overflow: hidden;
	}
	.cont2-b-item3{
		width: 100%;
		height: 50upx;
		display: flex;
		justify-content: space-between;
	}
	.cont2-b1-item3{
		font-size: 28upx;
		color: #FF3300;
		margin-top: 6upx;
	}
	.cont2-b2-item3{
		font-size: 36upx;
		color: #FF3300;
	}
	.demo_div { 
		left: 0;
		position: fixed; 
		bottom: 0; 
		width: 100%; 
	    } 
	.triangles{
		width:0;
		height:0;
		border-right:8upx solid transparent;
		border-left:8upx solid transparent;
		border-bottom:12upx solid #696969;
		display: inline-block;
	}
	.trianglex{
		width:0;
		height:0;
		border-right:8upx solid transparent;
		border-left:8upx solid transparent;
		border-top:12upx solid #696969;
		display: inline-block;
	}
</style>
