<template>
	<view class="index" >
		<view class="banner">	 
		<uni-swiper-dot :info="swiper.img" :current="current" :mode="mode" :dotsStyles="dotsstyle">
			<swiper class="bannerContent"  :autoplay="autoplay" :interval="interval" :duration="duration" @change="change">
				<swiper-item v-for="(value,index) in swiper.img" :key="index">
					<image :src="value" class="swiperImg"></image>
			
				</swiper-item>
			</swiper>
		</uni-swiper-dot>
		</view>
		
		<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
		
		<view class="banner">
			
			<li >
				<uni-icons custom-prefix="iconfont" type="icon-zhibo" size="70"></uni-icons>
				<br> 
				<font class="icontext">直播间</font>
			</li>
			
			<li >
				<uni-icons custom-prefix="iconfont" type="icon-jiaoliu" size="70"></uni-icons>
				<br>
				<font class="icontext">活动交流</font>
			</li>
			<li >
				<uni-icons custom-prefix="iconfont" type="icon-kecheng" size="70"></uni-icons>
				<br>
				<font class="icontext">课程</font>
				
			</li >
			<li>
				<uni-icons custom-prefix="iconfont" type="icon-huiyi" size="70"></uni-icons>
				<br>
				<font class="icontext">云乐会议</font>
			</li>
			
			
		</view>
		
		<view>
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
					selectedBackgroundColor:'#ff00ff',
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
						'../../static/img/1.jpeg',
						'../../static/img/2.jpeg',
						'../../static/img/3.jpeg'
					]
				},
				music:{
					title:"音乐信息",
					list:[
						{typec:"木管乐器1",typee:"Woodwind instrument1",src:"../../static/img/search.png"},
						{typec:"木管乐器2",typee:"Woodwind instrument2",src:"../../static/img/search.png"},
						{typec:"木管乐器3",typee:"Woodwind instrument3",src:"../../static/img/search.png"},
						{typec:"木管乐器4",typee:"Woodwind instrument4",src:"../../static/img/search.png"},
						{typec:"木管乐器5",typee:"Woodwind instrument5",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/search.png"}
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
		        }
		}
	}
</script>

<style lang="scss">
	
	.content {
		display:block;
		
		align-items: center;
		justify-content: center;
	}
	.icontext{
		color: #FF6034;
		face:"黑体";
	}
	li{
	margin-left: 20px;
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
		color:#ff557f;
		background-color: #f7ede2;
		.bannerContent{
			width: 90%;
			height: 320upx;
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
		background-color:#f7ede2 ;
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
