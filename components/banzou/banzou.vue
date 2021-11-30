<template>
	<view class="indexinall">
		<view v-for="(val,index) in result.list">
			<view class="yuepuitem">
				<image v-if="val.src" class="yuepuimg" :src="val.src"></image>
				<view class="yuepuinfo">
					<view>
						<view class="yuepuicon" > 伴奏</view>
						<font v-if="val.name" class="yueputitle">{{val.name}}</font>
					</view>
					
					<font v-if="val.musician" class="musician">{{val.musician}}</font>
			
					<font v-if="val.type" class="type">{{val.type}}</font>
				</view>
				<view class="shoucang">
					<font class="shoucangtext"> 收藏</font>
					<image class="collect" src="../../static/img/music/shoucang.png"></image>
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
				result:{
					title:"结果信息",
					list:[
						{name:"平调曲破",musician:"未知音乐人	",src:"../../static/img/music/music1.png",type:"图片谱"},
						{name:"平调曲破",musician:"音乐小星星",src:"../../static/img/music/music2.png",type:"图片谱"},
						
					
					]
				},
			}
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
.yuepuitem{
	padding-top: 45rpx;
	
	margin-right: 50rpx;
	margin-left: 50rpx;
	display: flex;
	flex-direction: row;
}
.yuepuinfo{
	margin-left: 30rpx;
	display: flex;
	flex-direction: column;
}
.yueputitle{
	letter-spacing: 15rpx;
	color: #FF7361;
}
.musician{
	font-size: 25rpx;
	color: #98989A;
	margin-top: 25rpx;
	letter-spacing: 5rpx;
}
	
.type{
	padding-top: 30rpx;
	line-height: 20rpx;
	font-size: 15rpx;
	color: #98989a;
	letter-spacing: 10rpx;
}
.yuepuimg{
	height: 150rpx;
	width: 150rpx;
}
.yuepuicon{
	display: inline;
	background-color: #e4b4aa;
	color: #FFFFFF;
	text-align: center;
	font-size: 10rpx;
	
	border-radius: 25rpx;
	padding:9rpx;
	padding-left: 15rpx;
	padding-right: 15rpx;
	margin-right: 20rpx;
}
.collect{
	position: relative;
	top: 10rpx;
	margin-left: 15rpx;
	height: 50rpx;
	width: 50rpx;
}
.shoucangtext{
	
	color: #0C0F27;
	font-size: 30rpx;
	
}
.shoucang{
	text-align: center;
	margin-left: auto;
	margin-top: auto;
	margin-bottom: auto;
	float:center;
}
.line{
		position: relative;
		
		margin-top:50rpx;
		
		margin-left: 55rpx;
		margin-right: 55rpx;

		height: 1px;
		background-color: rgba(231, 231, 237, 1.0);
		text-align: center;
		font-size: 16px;
	
		

	
		
	}
</style>
