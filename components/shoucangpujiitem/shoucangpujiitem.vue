<template>
	<view >
		<view class="index"> </view>
		<view v-for="(val,index) in result.list">
			<view class="yuepuitem">
				
				<image v-if="val.src" class="yuepuimg" :src="val.src"></image>
				<view class="yuepuinfo">
					<view>
						
						<font v-if="val.name" class="yueputitle">{{val.name}}</font>
					</view>
					
					<font v-if="val.musician" class="musician">{{val.musician}}</font>
			
					
				</view>
				<view class="shoucang">
					
					<image class="collect" src="../../static/img/threepoints.png"></image>
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
					title:"谱级信息",
					list:[
						{name:"何家营坐乐",musician:"创建:何忠信",src:"../../static/img/puji1.png"},
						{name:"何家营鼓乐",musician:"创建:小星星",src:"../../static/img/music/music1.png"},
						
					
					]
				},
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.index{

}
.yuepuitem{
	padding-top: 45rpx;
	
	margin-right: 50rpx;
	margin-left: 50rpx;
	display: flex;
	flex-direction: row;
}
.yuepuinfo{
	margin-top: auto;
    margin-bottom: auto;
	margin-left: 30rpx;
	display: flex;
	flex-direction: column;
}
.yueputitle{
	margin-top: auto;
	color: #000000;
}
.musician{
	font-size: 25rpx;
	color: #98989A;
	margin-top: 15rpx;
	letter-spacing: 5rpx;
}
	

.yuepuimg{
	height: 150rpx;
	width: 150rpx;
}

.collect{
	position: relative;
	top: 10rpx;
	margin-left: 15rpx;
	height: 50rpx;
	width: 50rpx;
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
