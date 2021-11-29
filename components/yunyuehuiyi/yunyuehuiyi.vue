<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="云乐会议" backgroundColor="#f8eee2" ></uni-nav-bar>
			
		<view class="hostinfo">
			<image class="headimg" src="../../static/img/follow1.png"></image>
			<view class="nameinfo">社员：何忠信</view>
			<image class="messageinfo" src="../../static/img/jx/likeempty.png"></image>
		</view>
		<view class="huiyicontent">
			<view class="huiyiicon">
				<view class="iconitem">
					<image class="bigicon" src="../../static/img/follow2.png"></image>
					<view class="huiyitext">加入会议</view>
				</view>
				<view class="iconitem">
					<image class="bigicon" src="../../static/img/follow2.png"></image>
					<view class="huiyitext">加入会议</view>
				</view>
				<view class="iconitem">
					<image class="bigicon" src="../../static/img/follow2.png"></image>
					<view class="huiyitext">加入会议</view>
				</view>
				
			</view>
			<view class='line'></view>
			<view class="lishihuiyi">历史会议></view>
			<view class="huiyiinfo">
				<view class="dateinfo">
					6月3日   今天
				</view>
				<view class="jutiinfo">
					2021年6月3日  14:00-16:30
				</view>
				<view class="otherinfo">
					何老师预定的会议
				</view>
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
.huiyiinfo{
	display: inline-block;
	margin:50rpx;
	margin-left:100rpx;
	margin-top: 10rpx;
	background-color: #f8eee2;
	padding:20rpx;
	padding-left: 30rpx;
	padding-right: 150rpx;
	border-radius: 45rpx;
	
}
.hostinfo{
	display: flex;
	flex-direction: row;
	margin: 20rpx;
}
.headimg{
	width: 100rpx;
	height: 100rpx;
}
.nameinfo{
	margin-top: auto;
	margin-bottom: auto;
	margin-left: 20rpx;
}
.messageinfo{
	width: 50rpx;
	height: 50rpx;
	float: right;
	margin-top: auto;
	margin-bottom: auto;
	margin-left: auto;
}
.huiyiicon{
	display: flex;
	flex-direction: row;
	margin-left: 50rpx;
	margin-right: 50rpx;
	

}
.dateinfo{
	font-size: 40rpx;
	letter-spacing: 5rpx;
	color: #000000;
	margin-top: 10rpx;
	margin-bottom: 10rpx;
}
.otherinfo{
	margin-top: 10rpx;
	margin-bottom: 10rpx;
	font-size: 30rpx;
	
}
.jutiinfo{
	color: #98989a;
	font-size: 20rpx;
	margin-top: 10rpx;
	margin-bottom: 10rpx;
}
.bigicon{
	width: 150rpx;
	height: 150rpx;
}
.iconitem{
	margin-top: 80rpx;
	margin-left:auto ;
	margin-right: auto;
	text-align: center;
}
.huiyicontent{
	background-color: #ffffff;
	height: 100%;
	width: 100%;
	border-top-left-radius: 55rpx;
	border-top-right-radius: 55rpx;
	position: absolute;
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
.lishihuiyi{
	margin: 40rpx;
	margin-left: 100rpx;
	background-color: #f0fbf7;
	display: inline-block;
	padding:5rpx;
	
	padding-left: 15rpx;
	padding-right: 15rpx;
	border-radius: 25rpx;
}
</style>
