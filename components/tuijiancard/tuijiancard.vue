<template>
	<view>
		<view class = "jxcard">
			<image src="../../static/img/douyin/19.png" class="jximg"></image>
			<view class="info">
				<view class="infotext">
					<font class="jxtitle">国风民乐!太好听了</font>
					<br>
					<font class="jxsubtitle">声色犬马</font>
				</view>
				<image src="../../static/img/follow1.png" class="likeimg"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"tuijiancard",
		data() {
			return {
				music:{
					title:"推荐信息",
					list:[
						{typec:"木管乐器1",typee:"Woodwind instrument1",src:"../../static/img/muguan.png"},
						{typec:"木管乐器2",typee:"Woodwind instrument2",src:"../../static/img/muguan.png"},
						{typec:"木管乐器3",typee:"Woodwind instrument3",src:"../../static/img/muguan.png"},
						{typec:"木管乐器4",typee:"Woodwind instrument4",src:"../../static/img/muguan.png"},
						{typec:"木管乐器5",typee:"Woodwind instrument5",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
						{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"}
					]
				},
			};
		}
	}
</script>

<style>
	.jxcard{
		margin-top: 300rpx;
		background-color: #ffffff;
		width: 300rpx;
		
	}
	.jxtitle{
		color: #0000FF;
		font-weight: bold;
		font-size: 10rpx;
		text-align: center;
	}
	.infotext{
		margin-left: 20rpx;
	}
	.jxsubtitle{
		font-weight: bold;
		font-size: 8rpx;
		color: #07C160;
	}
	.info{
		flex-direction: column;
	}
	.jximg{
		width: 300rpx;
		height: 400rpx;
		border-radius: 45rpx;
	}
		
	.likeimg{
		width: 50rpx;
		height: 50rpx;
		margin-top: 20rpx;
		margin-left: auto;
	}
	.infotext{
		width: 200rpx;
		background-color: #ffffff;
	}
	.info{
		flex-direction: row;
		
		display: flex;
	}
</style>
