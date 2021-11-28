<template>
	<view>
		<view class="top-swiper">
			 <view class="bg">
				 <view class="placeholder"></view>
				 <view class="image">
					 <image :src="swiper.list[swiper.index]" mode="aspectFill"></image>
				 </view>
			 </view>
			 <view class="box">
				<view style="height: 44px;"></view>
			 	<swiper class="swiper" :previous-margin="swiper.margin" :next-margin='swiper.margin' :circular="true" @change="swiperChange">
			 		<swiper-item v-for="(item,index) in swiper.list" @click="goUrl('/components/shangpinxiangqing/shangpinxiangqing')" >
						
			 			<image class='le-img' :src='item' :class="{'le-active':swiper.index == index}"></image>
						<image class='browsenum' src="/static/img/browsenum.png" :class="{'bn-active':swiper.index==index}"></image>
						
						<font class="browsenumval":style="">3.6K</font>
						<font class="instrumentname">16弦竖琴</font>
						<image class="storeheadpicture" src="/static/img/follow1.png" :class="{'le-active':swiper.index==index}"></image>
						<view class="storeinfo">
							<font class="storename" >班士顿专卖店</font>
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
			goUrl : function (str){
				uni.navigateTo({
					url: str
				});
			},
			
		}
	}
</script>

<style lang="scss">
	swiper-item{
		position: relative;
		display: flex;
		.browsenum{
			position: absolute;
			
		}
	}
	
.top-swiper{
		margin-bottom: 30rpx; 
		
		.bg{
			padding-top: var(--status-bar-height);
			box-sizing: content-box;
			width: 100%;
			position: relative;
			
			.placeholder{
				box-sizing: content-box;
				padding-top: 600rpx;
				height: 44px;
			}
			
			.image{
				box-sizing: content-box;
				position: absolute;
				z-index: 1;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				overflow: hidden;
				
				&::after{
					content: '';
					position: absolute;
					width: 100%;
					height: 100%;
					z-index: 1;
					bottom: 0;
					left: 0;
					height: 65%;
					background-image: linear-gradient(to bottom ,transparent, #F8EEE2);
				}
				
				> image{
					position: absolute;
					box-sizing: content-box;
					padding: 60px;
					top: 0;
					left: 0;
					width: 100%;
					height: 80%;
					top: -60px;
					left: -60px;
					filter: blur(50px);
				}
			}
		}
		
		.box{
			padding-top: var(--status-bar-height);
			box-sizing: content-box;
			position: absolute;
			z-index: 5;
			top: 0;
			left: 0;
			width: 100%;
			height: auto;
		}
			
		
		.swiper {
			height: 600rpx;
			margin: 0 20rpx;
			.browsenum{
				width: 30rpx;
				height: 20rpx;
				position: absolute;
				top:50rpx;
				left:40rpx;
				
			}
			.instrumentname{
				color: #0000FF;
				position: absolute;
				bottom: 140rpx;
				left:40rpx;
				font-weight: bold;
				font-size: 36rpx;
				
			}
			.storeinfo{
				position: absolute;
				bottom: 60rpx;
				left: 130rpx;
				
			}
			.storename{
				color:"#ff007f" !important;
				font-size: 28rpx;
				font-weight: bold;
				
				
			}
			.storeheadpicture{
				position: absolute;
				bottom: 35rpx;
				left:35rpx;
				height: 90rpx;
				width: 90rpx;
				
				
			}
			.browsenumval{
				position: absolute;
				top:45rpx;
				left:80rpx;
				font-weight: bold;
				font-size: 19rpx;
			}
			.le-img {
				width: 100%;
				height: 100%;
				display: block;
				
				border-radius: 4px;
				padding-right: 10rpx;
				padding-left: 10rpx;
				
			}
		
		}
	}
</style>
