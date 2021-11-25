<template>
	<view class="index">
		<view class="title" :class="topNavStyle.class" :style="topNavStyle.style">
			<view class="flex_col">
				<view class="box1"></view>
				<view class="flex_grow flex_col flex_center tab">
					<view v-for="(item,index) in topNavArr" :key="index"
					 :class="{ 'active':topNavIndex==index }" 
					 :data-index="index" @tap="changeTopNav">{{item}}</view>
				</view>
				<view class="box1 align_r">
					
				</view>
			</view>
		</view>
		<view v-if="topNavIndex==0">
		<card-swiper ></card-swiper>
		<view class="mailshowinfo">
			<font class="mailtitle">精选好物</font>
			<font class="viewall">View All</font>
		</view>
		<goodscard :prodata="goods"></goodscard>
		</view>
		<view v-if="topNavIndex==1">
		<jingxuan></jingxuan>
		</view>
		<view v-if="topNavIndex==2">
		<follow></follow>
		</view>	
		
	</view>
</template>

<script>
	import cardSwiper from '@/components/gradientnav/gradientnav';
	import jingxuan from '@/components/jingxuan/jingxuan';
	import follow from '@/components/follow/follow';
	import goodscard from '@/components/goodscard/goodscard';
	import tuijiancard from '@/components/tuijiancard/tuijiancard';
	export default {
		data() {
			
			return {
				topNavIndex:0,
				topNavArr:['商城','精选','关注'],
				pageScrollTop:0,	// 页面滚动距离
				goods:{
					title:"商品信息",
					list:[
						{name:"木管乐器1",storename:"Woodwind instrument1",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器2",storename:"Woodwind instrument2",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器3",storename:"Woodwind instrument3",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						
					]
				},
			}
			
		},
		components:{
			cardSwiper
		},
		computed:{
			topNavStyle(){
				let r = this.pageScrollTop  / 100;
				return {
					"class":r>=0.85?'style2':'',
					"style":`background-color: rgba(247, 237, 226,${r>=1?1:r});`
				}
			}
		},
		onPageScroll(e){
			this.pageScrollTop = Math.floor(e.scrollTop);
		},
		onShow() {
			this.topNavIndex=0;
		},
		methods: {
			// 顶部导航改变
			changeTopNav(e){
				this.topNavIndex = e.currentTarget.dataset.index;
				e.currentNumber();
			},
			// 去搜索
			toSearch(){
				uni.navigateTo({
					url:`/pages/search/search`  
				})
			}
		}
	}
</script>

<style lang="scss">
	@import "@/lib/global.scss";
	
	page{
		background-color: #ffe8e6;
	}
	/* 标题栏 */
	.title{
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: auto;
		padding-top: var(--status-bar-height);
		z-index: 10;
		
		
		&>view{
			height: 44px;
		}
		
		.box1{
			width: 60rpx;
			margin: 0 40rpx;
			font-size: 36rpx;
		}
		
		
		.tab{
			&>view{
				margin: 0 30rpx;
				line-height: 64rpx;
				font-size: 36rpx;
				position: relative;
				letter-spacing: 0;
				transition: transform 0.3s ease-in-out 0s;
				transform: scale(1,1);
				
				&.active{
					color: rgba(255,255,255,1);
					transform: scale(1.15,1.15);
				}
			}
		}
		
		&.style2{
			color: #55007f;
			background-color:#5555ff;
			
			.tab{
				&>view{
					&.active{
						color: #FFF;
					}
				}
			}
		}
	}
	.mailshowinfo{
		font-weight: bold;
		font-size: 36rpx;
		margin-top:80rpx;
		margin-left: 60rpx;
	
		
	}
	.viewall{
		
		display: inline;
		font-size: 10rpx;
		font-weight: lighter;
		margin-top:5rpx ;
		margin-left: auto;
		margin-right: 45rpx;
		float: right;
	}
	.index{
		background-color:#ffe8e6 ;
	}

</style>
