<template>
	<view>
		<view class="blurimg">
			<image  class="blurimgitem" src="../../static/img/huodongjiaoliu.png"></image>
		</view>
		<view class="huodongtitleinfo">
			<image class="huodongmaininfo" src="../../static/img/huodongjiaoliu.png"></image>
			<view class="textinfo">【西安站】2021全国巡演 · [ 筝乐传承，共谱华章 ]</view>
		</view>
		<view class="bottominfo">
			<view class="lineone">
				<image class="huodongicon" src="../../static/img/huodong/huodongtime.png"></image>
				<view class="shijiantext">2021年6月3日  14:00-16:30</view> 
				<view class="state">预定中></view>
			</view>
			<view class="linetwo">
				<image class="huodongicon" src="../../static/img/huodong/huodongdingwei.png"></image>
				<view class="pos">
					<view class="mainpos">
						新城区长缨西路99号胡家庙
					</view>
					<view class="subpos">
						丹尼尔奥莱国际二楼东侧
					</view>
				</view>
				<image class="dingweiicon" src="../../static/img/huodong/huodongdaohang.png"></image>
				
			</view>
			<view class="linethree">
				<image class="huodongicon" src="../../static/img/huodong/fuwubaozhang.png"></image>
				<view class="fuwutextinfo">
					<view class="mainpos">
						服务保障
					</view>
					<view class="subpos">
						票品保真 | 假一赔三 | 无票赔付 | 闪电转退
					</view>
				</view>
				
			</view>
			<view class="line"></view>
			<uni-list :border="false">
				
				<uni-list-item title="猜你喜欢" :border="false"/>
				<uni-list-item title="闽南传统音乐文化" :border="false" rightText="2021年6月20日  8:00-9:00" />
				
				<uni-list-item title="汉唐古典乐普及讲座"  rightText="2021年7月3日  9:00-11:30" />
				
				<uni-list-item title="何家营鼓乐线下票"  rightText="2021年7月3日  9:00-11:30" />
				
			</uni-list>
			
		</view>
		<view class="goods-carts">
			<uni-goods-nav :options="options" :fill="true" :button-group="buttonGroup" @click="onClick" @buttonClick="buttonClick"/>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniGoodsNav} from '@dcloudio/uni-ui';
	import {uniList} from '@dcloudio/uni-ui';
	import {uniListItem} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniList,
			uniListItem,
			uniNavBar,
			uniGoodsNav,
		},
		data() {
			return {
				options: [ {
					icon: 'heart',
					text: '收藏',
					info: 0
				}],
				buttonGroup: [{
						text: '立即预定',
						backgroundColor: '#e4b4aa',
						color: '#fff'
					},
				],
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.shijiantext{
	margin-left: 20rpx;
	font-size: 30rpx;
	color: #000000;
}
.pos{
	margin-left: 20rpx;
}
.mainpos{
	color: #000000;
	font-size: 30rpx;
}
.fuwutextinfo{
	margin-left: 20rpx;
}
.subpos{
	color:#98989a;
	font-size: 25rpx;
	margin-top: 10rpx;
}
.bottominfo{
	padding-top: 40rpx;
	border-radius: 45rpx;
	background-color: #ffffff;
	display: flex;
	flex-direction: column;
	height: 100%;
	position: absolute;
	width: 100%;
}
.huodongicon{
	margin-top: 5rpx;
	width: 40rpx;
	height: 40rpx;
}
.dingweiicon{
	width: 90rpx;
	height: 90rpx;
	float: right;
	margin-left: auto;
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
.blurimg{
	position: absolute;
	height: 100%;
	width: 100%;
	top: 0;
	z-index: -1;
	-webkit-filter: blur(5px);
	filter: blur(15px);
	transform: scale(1.2);


}
.blurimgitem{
	width: 1000rpx;
	height: 600rpx;
}
.huodongtitleinfo{
	padding-top: 200rpx;
	margin-left: 40rpx;
	margin-right: 40rpx;
	display: flex;
	flex-direction: row;
}
.huodongmaininfo{
	width: 300rpx;
	height: 350rpx;
}
.textinfo{
	padding-top:100rpx;
	width: 450rpx;
	padding-left:40rpx;
	font-size: 30rpx;
	color: #FFFFFF;
	letter-spacing: 5rpx;
}
.lineone{
	padding:40rpx;
	padding-bottom: 10rpx;
	display: flex;
	flex-direction: row;
}
.linetwo{
	padding:40rpx;
	padding-bottom: 10rpx;
	display: flex;
	flex-direction: row;
}
.linethree{
	padding:40rpx;
	padding-bottom: 10rpx;
	display: flex;
	flex-direction: row;
}
.state{
	float: right;
	margin-left: auto;
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
