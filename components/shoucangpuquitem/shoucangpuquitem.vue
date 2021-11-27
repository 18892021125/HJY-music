<template>
	<view>
		<view v-for="(val,index) in yuepilist.list">
			<view class="yuepuinfo">
				<view class="textinfo">
					
					<view v-if="val.name" class="yueputitle">{{val.name}}</view>
					<view v-if="val.type" class="yueputype">{{val.type}}</view>
				</view>
				<image class="playicon" src="../../static/img/music/playimg.png"></image>
				<image class="shoucangicon" src="../../static/img/threepoints.png"></image>
				
			</view>
			<view class="line"></view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				yuepilist:{
					title:"乐谱信息",
					list:[
						{name:"1. 南吕一枝花",type:"(北词)"},
						{name:"2. 哪吒令",type:"(耍曲)"},
						{name:"3. 双云锣起目",type:"(游声)"},
						{name:"4. 得胜令",type:"(南词)"},
						{name:"5. 正宫端正好",type:"(北词)"},
						{name:"6. 南吕一枝花",type:"(北词)"},
						
						{name:"7. 南吕一枝花",type:"(北词)"},
						{name:"8. 南吕一枝花",type:"(北词)"},
					
					]
				},
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.yuepulist{
		background-color: #ffffff;
		border-top-left-radius: 35rpx ;
		border-top-right-radius: 35rpx;
	}
	.yuepuinfo{
		width: 100%;
		display: flex;
		flex-direction: row;
		margin-top: 40rpx;
	}
	.textinfo{
		margin-left: 30rpx;
		display: flex;
		flex-direction: column;
		
	}
	.yueputitle{
		font-size: 35rpx;
		letter-spacing: 3rpx;
	}
	.playicon{
	
		float: right;
		margin-left: auto;
		height: 80rpx;
		width: 80rpx;
	}
	.shoucangicon{
		margin-left: 40rpx;
		margin-right: 40rpx;
		padding-left: 0;
		height: 80rpx;
		width: 80rpx;
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
	.yueputype{
		margin-left: 45rpx;
	}
</style>
