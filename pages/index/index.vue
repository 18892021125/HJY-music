<template>
	<view class="index" >
		<view class="banner">	 
		<uni-swiper-dot :info="swiper.img" :current="current" :mode="mode" :dotsStyles="dotsstyle">
			<swiper class="bannerContent"  :autoplay="autoplay" :interval="interval" :duration="duration" @change="change">
				<swiper-item v-for="(value,index) in swiper.img">
				
					<image :src="value" class="swiperImg"></image>
					<font class="imgtitle">开启传统音乐之旅</font>
					<font class="imgtext">何家营鼓乐欣赏</font>
					<image src="../../static/img/musicicon.png" class="swipericon" style="width: 35rpx;height: 35rpx;"></image>
					
				</swiper-item>
			</swiper>
		</uni-swiper-dot>
		</view>
		
		<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		
		<view class="banner">
			
			<li >
				<view  class="imageicon" @tap="goUrl('../zhibo/zhibo')">
				<image src="../../static/img/zhibo.png" style="width: 80rpx;height: 80rpx;"></image>
				<br> 
				
				</view>
				<font class="icontext">直播间</font>
			</li>
			
			<li >
				<view  class="imageicon" @tap="goUrl('/components/huodongjiaoliu/huodongjiaoliu')">
				<image src="../../static/img/jiaoliu.png" style="width: 80rpx;height: 80rpx;"></image>
				<br> 
				
				</view>
				<font class="icontext">活动交流</font>
			</li>
			<li >
				<view  class="imageicon" @tap="goUrl('/components/kechengdetail/kechengdetail')">
				<image src="../../static/img/kecheng.png" style="width: 60rpx;height: 80rpx;"></image>
				<br> 
				
				</view>
				<font class="icontext" >课程</font>
				
			</li >
			<li>
				<view  class="imageicon" @tap="goUrl('/components/yunyuehuiyi/yunyuehuiyi')">
				<image src="../../static/img/yunyuehuiyi.png" style="width: 80rpx;height: 80rpx;"></image>
				<br> 
				
				</view>
				<font class="icontext">云乐会议</font>
			</li>
			
			
		</view>
		
		<view>
			<view class="yuepufenlei">乐谱分类</view>
			<musicclassification :prodata="music"></musicclassification>
		</view>
		
		
	</view>
	
</template>

<script>
	import {uniSearchBar} from '@dcloudio/uni-ui'
	import {uniSwiperDot} from '@dcloudio/uni-ui'
	import {uniIcons} from '@dcloudio/uni-ui'
	export default {
		components:{uniSearchBar,
					uniSwiperDot,
					uniIcons,
					},
		data() {
			return {
				dotsstyle:{
					selectedBackgroundColor:'#ff7361',
					backgroundColor:'rgba(255, 170, 255, 0.3)',
				},
				current: 0,
				mode: 'round',
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
				imgSrc:'./static/img/',
				swiper:{
					autoplay:true,
					img:[
						'../../static/img/show1.png',
						'../../static/img/lunbo2.jpg',
						'../../static/img/lunbo3.jpg'
					]
				},
				music:{
					title:"音乐信息",
					list:[
						
					]
				},
			}
		},
		onReady() {
			
		},
		onLoad() {
			
			
		},
		onShow() {
			
			
		},
		methods: {
		change(e) {
		            this.current = e.detail.current;
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
		.imgtitle{
			position: absolute;
			top: 40upx;
			left:30upx;
			letter-spacing: 4rpx;
			color: #ffffff;
			
			font-size: 36rpx;
			
		}
		.imgtext{
			position: absolute;
			top: 87rpx;
			left:65upx;
			letter-spacing: 2rpx;
			color:#e3dbd9;
			font-family: pfj;
			margin-left: 10rpx;
			margin-bottom: 15rpx;
		}
		.swipericon{
			position: absolute;
			top: 90rpx;
			left:30upx;
		}
		
	}
	.yuepufenlei{
		margin:35rpx ;
		margin-top: 15rpx;
		font-size: 45rpx;
	}
	.content {
		display:block;
		
		align-items: center;
		justify-content: center;
	}
	.icontext{
		color: #000000;
		letter-spacing: 2rpx;
	
	}
	.imageicon{
		background-color: #ffffff;
		border-radius: 30rpx;
		padding: 25rpx;
	}
	li{
	margin: 20rpx;
	padding-top: 10rpx;
	width: 450rpx;
	display: block;
	float: left;
	list-style:none;
	text-align: center;


	}
	.interactiontext{
	position: absolute;
	}
	.interaction{
			
		
		display: inline;
	}
	.index{
		width: 100vw;
		
		flex-direction: row;
		
		background-color: #F8EEE2;
		.bannerContent{
			width: 90%;
			height: 360rpx;
			margin:0 auto;
			.swiperImg{
				width: 100%;
				height: 100%;
				border-radius:20px;
			
			
			}
		}
	}
	
	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}
	.banner{
		background-color:#F8EEE2 ;
		display: flex;
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
