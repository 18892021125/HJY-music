<template>
	<view class="index">
		<view class="title">发现更多</view>
		<view class="subtitle">这里还有更多功能哦！</view>
		<view class="gongju">
			<view class="title">
				工具
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/tiaoyinqi.png"></image>
				<view class="type">调音器</view>
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/jiepaiqi.png"></image>
				<view class="type">节拍器</view>
				<switch class="switchitem" checked @change="switch1Change" />
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/daojishi.png"></image>
				<view class="type">倒计时</view>
				<switch class="switchitem" checked @change="switch1Change" />
			</view>
			<view class="title">
				其他
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/shouacng.png"></image>
				<view class="type">收藏</view>
				<switch class="switchitem" checked @change="switch1Change" />
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/fenxiang.png"></image>
				<view class="type">分享</view>
			</view>
			<view class="gongjuitem">
				<image class="icon" src="../../static/img/yuepumore/jubao.png"></image>
				<view class="type">举报</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.title{
	font-size: 50rpx;
	margin-top:40rpx;
	margin-left: 40rpx;
	color: #000000;
}
.subtitle{
	font-size: 30rpx;
	margin-left:40rpx ;
	margin-top: 10rpx;
	color: #e0e0e0;
}
.icon{
	width: 60rpx;
	height: 60rpx;
	
	margin-left: 40rpx;
	margin-top:30rpx;
	margin-bottom: 30rpx;
}
.gongju{

	margin-top: 50rpx;
	
	display: flex;
	flex-direction: column;
}
.gongjuitem{
	display: flex;
	flex-direction: row;
}
.title{
	font-size: 40rpx;
	margin-top: 50rpx;
	margin-bottom: 20rpx;
	color:#98989a;
}
.type{
	margin-bottom: 30rpx;
	margin-top: 40rpx;
	color: #000000;
	letter-spacing: 5rpx;
	margin-left: 20rpx;
}
.switchitem{
	float: right;
	margin-left: auto;
	margin-right: 200rpx;
	margin-top: 40rpx;
}
</style>
