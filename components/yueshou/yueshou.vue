<template>
	<view class="indexinall">
		<image class="empty" src="../../static/img/music/musicempty.png"></image>
		<view class="emptytext">空空如也</view>
	</view>
</template>

<script>
	export default {
		data() {
		},
		methods: {
			
		}
	}
</script>

<style>

.indexinall{
	background-color: #ffffff;
	margin-top: 50rpx;
	border-top-right-radius: 85rpx;
	border-top-left-radius: 85rpx;
	height:100%; 
	width: 100%;
	position:absolute; 
}
.empty{
	padding-top: 200rpx;
	display: block;
	margin: auto;
	width: 300rpx;
	height: 190rpx;
}
.emptytext{
	margin: auto;
	border-radius: 40rpx;
	margin-top: 200rpx;
	padding: 20rpx;
	padding-left: 50rpx;
	padding-right: 50rpx;
	width: 200rpx;
	letter-spacing: 4rpx;
	font-size: 35rpx;
	color:#FFFFFF;
	background-color: #e4b4aa;
	text-align: center;
}
</style>
