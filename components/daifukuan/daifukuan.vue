<template>
	<view>
		<view class="goodslist">
			<view class="gooditem">
				<image class="goodimg" src="../../static/img/douyin/19.png"></image>
				<view class="goodinfo">
					<view class="goodname">班士顿单板莱雅琴小竖琴十弦小众乐器便携式七弦小型里拉琴</view>
					<view class="goodprice">¥：9999元</view>
					<view class="actionbutton">
						<view class="cancel">取消</view>
						<view class="fukuan">付款</view>
					</view>
				</view>
				
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
.goodslist{
	margin-top: 100rpx;
}
.gooditem{
	display: flex;
	flex-direction: row;
	margin: 30rpx;
}
.goodname{
	margin-left: 15rpx;
	max-width: 500rpx;
}
.goodimg{
	width: 180rpx;
	height: 200rpx;
	min-width: 180rpx;
}
.goodinfo{
	display: flex;
	flex-direction: column;
	min-width: 400rpx;
}
.goodprice{
	float: right;
	margin-left: auto;
	margin-top: auto;
	color: #ff7361;
}
.actionbutton{
	display: flex;
	flex-direction: row;
	float: right;
	margin-left: auto;
	margin-top: auto;
}
.cancel{
	background-color: #e4b4aa;
	padding-left: 15rpx;
	padding-right: 15rpx;
	border-radius: 15rpx;
	padding-top:5rpx;
	padding-bottom: 5rpx;
	margin-right: 40rpx;
	color: #FFFFFF;
}
.fukuan{
	background-color: #cae3da;
	padding-left: 15rpx;
	padding-right: 15rpx;
	padding-top:5rpx;
	padding-bottom: 5rpx;
	border-radius: 15rpx;
	color: #FFFFFF;
}
.line{
		position: relative;
		margin-top:50rpx;
		margin-left: 35rpx;
		margin-right: 35rpx;
		height: 1px;
		background-color: rgba(231, 231, 237, 1.0);
		text-align: center;
		font-size: 16px;
	}
</style>
