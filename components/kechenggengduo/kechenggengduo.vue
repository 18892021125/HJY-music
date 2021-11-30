<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="课程" backgroundColor="#f8eee2" ></uni-nav-bar>
		<image class="mainimg" src="../../static/img/kecheng2.png"></image>
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="goumaitip">
			<view class="kechengname">
				<view class="mainname">坐乐之鼓篇</view>
				<view class="subname">何家营乐社-非遗重点乐器</view>
			</view>
			<view class="timeinfo">开课时间： 2021年11月25日-2021年12月25日</view>
			<view class="goumaiinfo">
				<view class="price">
					¥：666元
				</view>
				<view class="goumaiicon">
					立即购买
				</view>
			</view>
		</view>
		<view class="kechenginfo">
			<view class="kechengneirong">课程内容</view>
			<view  v-for="(val,index) in kecheng.list">
				<view v-if="val.name" class="xiaojieneirong">
					<view class="xiaojiename">{{val.name}}</view>
					<image class="playicon" src="../../static/img/music/playimg.png" @click="goUrl('/components/kechengxiangqingsiji/kechengxiangqingsiji')"></image>
				</view>
				<view class="line"></view>
			</view>
			
			
		</view>
	</view>
</template>

<script>
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import {uniNavBar} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniSegmentedControl,
			uniNavBar,
		},
		data() {
			return {
				items: ['课程购买','课程介绍','课程评价'],
				current: 0,
				colorIndex: 0,
				activeColor: '#ff7361',
				styleType: 'text',
				kecheng:{
					title:"课程信息",
					list:[
						{name:"第一节：乐社简介"},
						{name:"第二节：鼓乐的音乐之美"},
						{name:"第三节：掌握鼓乐技法"},
						{name:"第四节：音准的控制"},
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
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
			goUrl : function (str){
				uni.navigateTo({
					url: str
				});
			},
		}
	}
</script>

<style lang="scss">
page{
	background-color: #f8eee2;
}
.playicon{
	width: 80rpx;
	height: 80rpx;
	float: right;
	margin-left: auto;
	margin-right: 30rpx;
}
.xiaojieneirong{
	display: flex;
	flex-direction: row;
}
.kechenginfo{
	margin:30rpx;
	background-color: #FFFFFF;
	border-radius: 45rpx;
	display: flex;
	flex-direction: column;
}
.kechengneirong{
	margin:20rpx;
	padding-top: 30rpx;
	color:#000000;
	font-size: 32rpx;
}
.xiaojiename{
	margin: 20rpx;
	font-size: 35rpx;
}
.goumaitip{
	margin:30rpx;
	background-color: #FFFFFF;
	display: flex;
	flex-direction: column;
	border-radius: 45rpx;
}
.kechengname{
	display: flex;
	flex-direction: row;
	margin:20rpx;
	margin-top: 35rpx;
	
}
.mainname{
	color: #000000;
	font-size: 35rpx;
	letter-spacing: 5rpx;
}
.subname{
	color:#98989a;
	letter-spacing: 4rpx;
	margin-top: auto;
	margin-bottom: auto;
	margin-left: 20rpx;
}
.timeinfo{
	margin:20rpx;
	font-size: 20rpx;
	color: #98989a;
}
.goumaiinfo{
	display: flex;
	flex-direction: row;
	margin: 20rpx;
	margin-bottom: 30rpx;
}
.goumaiicon{
	background-color: #e4b4aa;
	float: right;
	margin-left: auto;
	padding-left: 20rpx;
	padding-right: 20rpx;
	padding-top:8rpx;
	padding-bottom: 5rpx;
	border-radius: 35rpx;
	color:#FFFFFF;
	text-align: center;
	
}
.price{
	color:#ff8879;
	font-size: 40rpx;
}
.mainimg{
	display: flex;
	margin-left:auto;
	margin-right: auto;
	margin-bottom: 20rpx;
	width: 90%;
	height: 360rpx;
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
