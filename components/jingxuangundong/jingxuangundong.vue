<template>
	<view>
		<view class="top-swiper">
		
			 <view class="box">
				
			 	<swiper class="swiper" :previous-margin="swiper.margin" :next-margin='swiper.margin' :circular="true" @change="swiperChange">
			 		<swiper-item v-for="(item,index) in swiper.list" :key="index">
						
			 			<image class='le-img' :src='item' :class="{'le-active':swiper.index == index}"></image>
						<view class="imginfo">
							<text class="imgtitle" >丝竹鼓乐沪上盛典</text>
							<br>
							<text class="more">more></text>
						</view>
					</swiper-item>
			 	</swiper> 
			 </view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiper: {
					margin: "150rpx",
					index: 0,
					list: [
						"/static/img/douyin/7.jpg",
						"/static/img/douyin/19.png",
						"/static/img/douyin/20.png",
					]
				}
			}
		},
		components: {
	
		},
		mounted() {
	
		},
		methods: {
			//swiper滑动事件
			swiperChange: function(e) {
				this.swiper.index = e.detail.current;
			},
		}
	}
</script>

<style lang="scss">

	.imginfo{
		position: absolute;
		top:20rpx;
		left:40rpx;
		
		.imgtitle{
			font-size:25rpx ;
			font-weight: bold;
			color: "#5555ff";
		}
	
	}
	.top-swiper{
			
			background-color:#ffe8e6 ;
			
			.box{
				background-color:#ffe8e6 ;
				
				
				z-index: 1;
				top: 0;
				left: 0;
				width: 100%;
				height: 300rpx;
			}
				
			
				
			.le-img {
				width: 400rpx;
				height: 300rpx;
				display: block;
				background-color:#ffe8e6 ;
				margin-left:5rpx ;
				margin-right:5rpx;
			
				
				border-radius:50rpx;
			}
			.swiper {
				
				
		
			
			}
		}
</style>

