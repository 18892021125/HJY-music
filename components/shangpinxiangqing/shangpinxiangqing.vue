<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="商品详情" backgroundColor="#f8eee2" ></uni-nav-bar>
		<view class="goodsinfo">
			<image class="goodsimg" src="../../static/img/goods/goodsinfo1.png"></image>
			<view class="goodstextinfo">
				<view class="huodongtitle">狂欢不止</view>
				<view class="priceinfo">
					<view class="price">$: 168-880元</view>
					<view class="originprice"> 价格 $:666起</view>
				</view>
				<view class="jifen">
					<view class="tip">购买得积分</view>
					<view class="more">查看 > </view>
				</view>
				<view class="goodname">班士顿单板莱雅琴小竖琴十弦小众乐器便携式七弦小型里拉琴lyre琴</view>
				<view class="vip">会员优享：注册会员享0元下单，先试后付</view>
			</view>
			
		</view>
		<view class="goods-carts">
			<uni-goods-nav :options="options" :fill="true" :button-group="buttonGroup" @click="onClick" @buttonClick="buttonClick"/>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniGoodsNav} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniNavBar,
			uniGoodsNav,
		},
		data() {
			return {
				options: [{
					icon: 'chat',
					text: '客服'
				}, {
					icon: 'shop',
					text: '店铺',
					info: 0,
					infoBackgroundColor:'#007aff',
					infoColor:"#f5f5f5"
				}, {
					icon: 'star',
					text: '收藏',
					info: 0
				}],
				buttonGroup: [{
						text: '加入购物车',
						backgroundColor: '#e4b4aa',
						color: '#fff'
					},
					{
						text: '立即购买',
						backgroundColor: '#cae3da',
						color: '#fff'
					}
				],
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
.goodstextinfo{
	background-color: #ffffff;
	margin:40rpx;
	margin-top:20rpx;
	display: flex;
	flex-direction: column;
	border-radius: 45rpx;
	
}
.huodongtitle{
	margin-left: 20rpx;
	margin-top:40rpx;

	color:#ff7361;
	font-size: 30rpx;
}
.jifen{
	display: flex;
	flex-direction: row;
}
.more{
	float: right;
	margin-left: auto;
	font-size: 20rpx;
	margin-right: 15rpx;
	color:#98989a
}
.goodsimg{
	margin: 40rpx;
	width: 670rpx;
	height: 850rpx;
}
.priceinfo{
	display: flex;
	flex-direction: row;
}
.price{
	margin-left: 20rpx;
	margin-top:30rpx;
	margin-bottom: 30rpx;
	color: #ff7361;
	font-size: 40rpx;
}
.originprice{
	margin-left: 40rpx;
	margin-top:40rpx;
	margin-bottom: 30rpx;
	color:#98989a;
	text-decoration:line-through;
}
.tip{
	margin-left: 20rpx;
	padding-left: 20rpx;
	padding-right: 20rpx;
	padding-top: 5rpx;
	padding-bottom: 5rpx;
	border-radius: 15rpx;
	color: #FFFFFF;
	background-color: #e4b4aa;
}
.goods-carts {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: column;
		position: fixed;
		left: 0;
		right: 0;
		/* #ifdef H5 */
		left: var(--window-left);
		right: var(--window-right);
		/* #endif */
		bottom: 0;
	}
.goodname{
	margin:20rpx;
	margin-top: 40rpx;
	margin-bottom: 40rpx;
	letter-spacing: 4rpx;
	line-height: 50rpx;
}
.vip{
	background-color: #f8eee2;
	margin-left: auto;
	margin-right: auto;
	padding-top:5rpx;
	padding-bottom: 5rpx;
	color:#c4af81;
	padding-left: 50rpx;
	padding-right: 50rpx;
	border-radius: 35rpx;
	margin-bottom: 35rpx;
}
</style>
