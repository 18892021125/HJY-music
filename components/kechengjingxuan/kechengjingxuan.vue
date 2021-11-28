<template>
	<view>
		<image class="mainimage" src="../../static/img/jingxuankechengtu.png"></image>
		<view class="zuijinzhibo">
			<view class="titleinfo">
				<view class="zuijinzhibotitle">最近直播</view>
				<image class="zhiboicon" src="../../static/img/zhibo.png"></image>
			</view>
			<view class="zhiboitem">
				<image class="headimg" src="../../static/img/zhiboyuan2.png"></image>
				<view class="textinfo">
					<view class="nameandtype">何忠信 —— 鼓乐团演奏</view>
					<view class="zhibodate">2021年11月22日 19:00-20:30</view>
				</view>
				
			</view>
			<view class="zhiboitem">
				<image class="headimg" src="../../static/img/zhiboyuan1.png"></image>
				<view class="textinfo">
					<view class="nameandtype">何洪斌 —— 坐乐乐谱解读</view>
					<view class="zhibodate">2021年11月25日 19:00-20:30</view>
				</view>
			</view>
		</view>
		<view class="kechenggoumai">
			<view class="titleinfo">
				<view class="zuijinzhibotitle">课程购买</view>
			</view>
			<view class="kechengitem">
				<image class="kechengimg" src="../../static/img/kecheng2.png"></image>
				<view class="textinfo">
					<view class="nameandtype">坐乐之鼓篇</view>
					<view class="zhibodate">何家营鼓乐设</view>
				</view>
				<view class ="more">
					<view class="moretext" @click="goUrl('/components/kechenggengduo/kechenggengduo')">更 多</view>
					<view class="canjiarenshu">329人参加</view>
				</view>
			</view>
			<view class="line"></view>
			<view class="kechengitem">
				<image class="kechengimg" src="../../static/img/kecheng1.png"></image>
				<view class="textinfo">
					<view class="nameandtype">坐乐之笛篇</view>
					<view class="zhibodate">何家营鼓乐设</view>
				</view>
				<view class ="more">
					<view class="moretext" @click="goUrl('/components/kechenggengduo/kechenggengduo')">更 多</view>
					<view class="canjiarenshu">417人参加</view>
				</view>
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
			goUrl : function (str){
				uni.navigateTo({
					url: str
				});
			},
		}
	}
</script>

<style lang="scss">
.mainimage{
	height:300rpx;
	width: 700rpx;
	margin: 25rpx;
	
}
.kechengimg{
	width: 200rpx;
	height: 80rpx;
	margin:40rpx;
	
	
}
.titleinfo{
	
	padding-top: 50rpx;
	padding-left:30rpx;
	display: flex;
	flex-direction: row;
}
.zuijinzhibo{
	background-color: #ffffff;
	border-radius: 35rpx;

	margin: 30rpx;
}
.kechenggoumai{
	background-color: #FFFFFF;
	margin: 30rpx;
	border-radius: 35rpx;
}
.zhiboicon{
	width: 50rpx;
	height: 40rpx;
	margin-left: 30rpx;
}
.zhiboitem{
	display: flex;
	flex-direction: row;
}
.kechengitem{
	display: flex;
	flex-direction: row;
}
.headimg{
	height: 100rpx;
	width: 100rpx;
	margin:30rpx
}
.textinfo{
	
	margin: 30rpx;
	margin-top: 35rpx;
	margin-left: 10rpx;
}
.zhibodate{
	font-size: 20rpx;
	color: #e0e0e0;
	letter-spacing: 2rpx;
}
.nameandtype{
	font-size: 35rpx;

	letter-spacing: 4rpx;
	
}
.zuijinzhibotitle{
	letter-spacing: 5rpx;
}
.moretext{
	background-color: #e4b4aa;
	border-radius:45rpx ;
	color: #ffffff;
	padding-top: 5rpx;
	padding-bottom: 5rpx;

}
.more{
	text-align: center;
	margin-top: 30rpx;
	margin-left: 10rpx;
	font-size: 25rpx;
	
}
.canjiarenshu{
	font-size: 15rpx;
	
	margin: 10rpx;
	color: #e0e0e0;
}
.line{
	position: relative;
	margin-top:10rpx;
	margin-left: 55rpx;
	margin-right: 55rpx;
	height: 1px;
	background-color: rgba(231, 231, 237, 1.0);
	text-align: center;
	font-size: 16px;
}
</style>
