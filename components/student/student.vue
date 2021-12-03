<template>
	<view class="userindex">
		<view class="teacherview">
			<view class="userinfo">
				<image src="../../static/img/xeyuantouxiang.jpg" style="width: 70rpx;height: 70rpx;border-radius: 50%;" class="headimg"></image>
				<view class="textinfo">
					<font class="username">Carly Rae Jepasen</font>
					<font class="sign">View Profile</font>
				</view>
			</view>
			<view class="topoption">
				<view class="topitem"  @click="goUrl('/components/followcard/followcard')">关注</view>
				<view class="topitem" @click="goUrl('/components/puqushoucang/puqushoucang')">收藏</view>
				<view class="topitem" @click="goUrl('/components/fans/fans')">粉丝</view>
			</view>
			<view class="line"></view>
			<view class="useroption">
				
				<view class="optionitem" @click="goUrl('/components/message/message')">
					<image src="../../static/img/xiaoxi.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">消息</font>
					</view>
				</view>
				
				<view class="optionitem" @click="goUrl('/components/lixianhuancun/lixianhuancun')">
					<image src="../../static/img/shezhi.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">离线缓存</font>
					</view>
				</view>
				<view class="optionitem"  @click="goUrl('/components/timetableindex/timetableindex')">
					<image src="../../static/img/wodekecheng.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">我的课程</font>
					</view>
				</view>
				
				
				
				<view class="optionitem" @click="goUrl('/components/wodedingdan/wodedingdan')">
					<image src="../../static/img/dingdan.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">订单</font>
					</view>
				</view>
				
				
			</view>
			<view class="line"></view>
			<view class="kefu" @click="goUrl('/components/kefu/kefu')">
				
				<image src="../../static/img/lianxikefu.png" style="width: 50rpx;height: 50rpx;"></image>
				<view class="kefuoptiontext">
					<font >联系客服</font>
				</view>
			</view>
			<view class="line"></view>
			<view class="quitbutton">
				<van-button  round icon="../../static/img/quiticon.png" type="primary" >
				  退出账户
				</van-button>
			</view>
			</view>
	</view>
</template>

<script>
	export default {
		name:"teacher",
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
	.topoption{
		margin-top: 40rpx;
		display: flex;
		flex-direction: row;
	}
	.topitem{
		width: 33%;
		text-align: center;
		
	}
	.teacherview{
		margin-top: 150rpx;
		background-color: #ffffff;
		border-top-right-radius: 45rpx;
		border-top-left-radius: 45rpx;
		height: 100%;
		width: 100%;
		
	}
	.quitbutton{
		position: relative;
		margin-bottom: auto;
		margin-left: 37rpx;
	}
	.kefu{
		margin-top:47rpx ;
		padding-left: 50rpx;
		display: flex;
		flex-direction: row;
		padding-bottom: 17rpx;
	}
	.optiontextv{
		margin-top:auto ;
		margin-left: 37rpx;
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
	.userindex{
		height: 100%;
		background-color: #f8eee2;
		height:100%;
		width: 100%;
		position:absolute; 
	}
	.useroption{
		display: flex;
		flex-direction: column;
		padding-left: 50rpx;
		padding-top: 20rpx;
		padding-bottom: 20rpx;
	}
	.userinfo{
		display: flex;
		flex-direction: row;
		padding-left:50rpx ;
		padding-top: 50rpx;
	}
	.kefuoptiontext{
		margin-top:auto ;
		margin-left: 37rpx;
		margin-bottom: auto;
		
	}
	.textinfo{
		padding-left: 47rpx;
		flex-direction: column;
		display: flex;
	}
	.optionitem{
		padding-top: 37rpx;
		padding-bottom: 37rpx;
		display: flex;
		flex-direction: row;
	}
	.username{
		font-weight: bold;
		font-family: "Poppins";
	}
</style>
