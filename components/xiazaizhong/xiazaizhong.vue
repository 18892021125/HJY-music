<template>
	<view>
		<view class="downloadinglist">
			<view class="downloaditem">
				<view class="index">1</view>
				<image class="downloadimg" src="../../static/img/kecheng1.png"></image>
				<view class="downname">何家营鼓乐课程</view>
				<image class="downinfo" src="../../static/img/xiazaizhong.png"></image>
			</view>
			<view class="line"></view>
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
.downloaditem{
	display: flex;
	flex-direction: row;
	margin: 30rpx;
}
.downloadimg{
	width: 220rpx;
	height: 100rpx;
	margin-left: 20rpx;
}
.index{
	margin-top: auto;
	margin-bottom: auto;
	color: #e4b4aa;
}
.downinfo{
	float: right;
	margin-left: auto;
	width: 50rpx;
	height: 50rpx;
	margin-top: auto;
	margin-bottom: auto;
}
.downname{
	margin-left: 15rpx;
	margin-top:auto;
	margin-bottom: auto;
}
.line{
		position: relative;
		
		margin-top:37rpx;
		
		margin-left: 35rpx;
		margin-right: 35rpx;
		margin-bottom: 35rpx;
		height: 1px;
		background-color: rgba(239, 239, 243, 1.0);
		text-align: center;
		font-size: 16px;
		color: rgba(239, 239, 243, 1.0);
		

	
		
	}
</style>
