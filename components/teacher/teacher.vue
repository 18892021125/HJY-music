<template>
	<view class="userindex">
		<view class="teacherview">
			<view class="userinfo">
				<image src="../../static/img/follow1.png" style="width: 70rpx;height: 70rpx;" class="headimg"></image>
				<view class="textinfo">
					<font class="username">Jenat Ara</font>
					<font class="sign">View Profile</font>
				</view>
			</view>
			<view class="line"></view>
			<view class="useroption">
				<view class="optionitem" @click="goUrl('/components/followcard/followcard')">
					<image src="../../static/img/tongxunlu.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">通讯录</font>
					</view>
				</view>
				<view class="optionitem">
					<image src="../../static/img/xiaoxi.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">消息</font>
					</view>
				</view>
				<view class="optionitem" @click="goUrl('/components/puqushoucang/puqushoucang')">
					<image src="../../static/img/puqushoucang.png"  style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">谱曲收藏</font>
					</view>
				</view>
				<view class="optionitem" @click="goUrl('/components/settings/settings')">
					<image src="../../static/img/shezhi.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">设置</font>
					</view>
				</view>
				<view class="optionitem"  @click="goUrl('/components/timetableindex/timetableindex')">
					<image src="../../static/img/pailianshijianbiao.png" style="width: 50rpx;height: 50rpx;"></image>
					<view class="optiontextv">
						<font class="optiontext">排练时间表</font>
					</view>
				</view>
				
			</view>
			<view class="line"></view>
			<view class="kefu" @click="goUrl('/components/kefu/kefu')">
				
				<image src="../../static/img/lianxikefu.png" style="width: 50rpx;height: 50rpx;"></image>
				<view class="kefuoptiontext">
					<font >客服</font>
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
		background-color: rgba(145, 148, 174, 1.0);
		text-align: center;
		font-size: 16px;
		color: rgba(145, 148, 174, 1.0);
		

	
		
	}
	.userindex{
		height: 100%;
		background-color: #ffffff;
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
