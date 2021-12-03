<template>
	
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="木管乐器" backgroundColor="#f8eee2" ></uni-nav-bar>
		<view class="maininfo">
			<image class="imageinfo" src="../../static/img/muguan.png" ></image>
			<view class="maintextinfo"> 木管乐器包括长笛,短笛,双簧管,单簧管,萨克斯,排萧和低音管,他们都有一个可以吹出空气的中空管子。木管乐器的得名是由于它们起初都是木制的,但是现在许多木管乐器也用金属和塑料制造。<i></i></view>
		</view>
		<view style="padding-bottom: 100rpx;">
			<view class="shoucang">
				<font class="shoucangtext"> 收藏</font>
				<image class="collect" src="../../static/img/music/shoucang.png"></image>
			</view>
		</view>
		<view class="yuepulist">
			<view v-for="(val,index) in yuepilist.list">
				<view class="yuepuinfo">
					<view class="textinfo">
						
						<view v-if="val.name" class="yueputitle">{{val.name}}</view>
						<view v-if="val.type" class="yueputype">{{val.type}}</view>
					</view>
					<image class="playicon" src="../../static/img/music/playimg.png"></image>
					<image class="shoucangicon" src="../../static/img/music/shoucangcircle.png"></image>
					
				</view>
				<view class="line"></view>
			</view>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniNavBar,
		},
		data() {
			return {
				yuepilist:{
					title:"乐谱信息",
					list:[
						{name:"1. 南吕一枝花",type:"(北词)"},
						{name:"2. 哪吒令",type:"(耍曲)"},
						{name:"3. 双云锣起目",type:"(游声)"},
						{name:"4. 得胜令",type:"(南词)"},
						{name:"5. 正宫端正好",type:"(北词)"},
						{name:"6. 南吕一枝花",type:"(北词)"},
						
						{name:"7. 南吕一枝花",type:"(北词)"},
						{name:"8. 南吕一枝花",type:"(北词)"},
					
					]
				},
			}
		},
		methods: {
			
			back() {
				uni.navigateBack({
					delta: 1
				})
			},
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #f8eee2;
	}	
	.yuepulist{
		background-color: #ffffff;
		border-top-left-radius: 35rpx ;
		border-top-right-radius: 35rpx;
	}
	.title{
		text-align: center;
		font-size: 40rpx;
		padding-bottom: 40rpx;
	}	
	.maintextinfo{
		padding-top: 20rpx;
		margin-right: 20rpx;
		width: 400rpx;
		text-align: justify;
		letter-spacing: 1rpx;
	}
	
	.maininfo{
		margin-top: 20rpx;
		text-indent:45rpx;
		display: flex;
		flex-direction: row;
		font-size: 28rpx;
	}
	.imageinfo{
		margin: 25rpx;
		width:300rpx;
		height: 300rpx;
	}
	.shoucangtext{
		color: #959595;
		font-size: 30rpx;
	}
	.shoucang{
		text-align: center;
		display: inline-block;
		float: right;
		padding-right: 30rpx;
		margin-bottom: 100rpx;
	}
	.collect{
		position: relative;
		top: 10rpx;
		margin-left: 15rpx;
		height: 50rpx;
		width: 50rpx;
	}
	.line{
		position: relative;
		margin-top:50rpx;
		margin-left: 55rpx;
		margin-right: 55rpx;
		height: 1px;
		background-color: rgba(231, 231, 237, 1.0);
		text-align: center;
		font-size: 16px;
	}
	.yuepuinfo{
		width: 100%;
		display: flex;
		flex-direction: row;
		margin-top: 40rpx;
	}
	.shoucangicon{
		margin-left: 40rpx;
		margin-right: 40rpx;
		padding-left: 0;
		height: 80rpx;
		width: 80rpx;
	}
	.playicon{
	
		float: right;
		margin-left: auto;
		height: 80rpx;
		width: 80rpx;
	}
	.textinfo{
		margin-left: 30rpx;
		display: flex;
		flex-direction: column;
		
	}
	.yueputitle{
		font-size: 35rpx;
		letter-spacing: 3rpx;
	}
	.yueputype{
		margin-left: 45rpx;
	}
</style>
