<template>
	<view>
		<view class="goods" v-for="(val,index) in prodata.list" :key="index" @tap="goUrl('./pages/user/user')">
			<view class="goodsitem">
				<image v-if="val.src" :src="val.src" style="width: 70px; height: 70px;margin-top: 15rpx;margin-left: 15rpx;margin-bottom: 15rpx; ">
				<view class="textinfo">
					<br>
					<font v-if="val.name" class="goodsname">{{val.name}}</font>
				    
					<font v-if="val.storename" class="storename">{{val.storename}}</font>
					
				</view>
				<view class="costcard" v-if="val.cost">
					<font class="type">¥：</font>
					<font class="number">{{val.cost}}</font>
					
				</view>		
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		
		data() {
			return {
				prodata:{
					title:"商品信息",
					list:[
						{name:"金镲",storename:"十三行乐器",src:"../../static/img/goods/jinca.png",cost:"56元"},
						{name:"木管",storename:"弘艺乐器旗舰店",src:"../../static/img/muguan.png",cost:"256元"},
						{name:"笙",storename:"弘艺乐器旗舰店",src:"../../static/img/goods/sheng.png",cost:"2680元"},
						{name:"竹笛",storename:"笛韵音行",src:"../../static/img/goods/zhudi.png",cost:"598元"},
			
						
					]
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
.textinfo{
	margin-left: 20px;
	display: flex;
	flex-direction: column;
}
.costcard{
	background-color: #ffe9e6;
	display: inline;
	padding:15rpx ;
	border-radius: 50rpx;
	margin-top: auto;
	margin-bottom: auto;
	margin-left: auto;
	margin-right: 19rpx;
	float: right;
	min-width: 160rpx;
	text-align: center;
	color: #ff7361;

}
.number{
	float: right;
}
.type{
	color: #FF6034;
	face:"黑体";
	float: left;
}
.name{
	font-weight: bold;
	margin-bottom:10rpx ;
	color: #000000 !important;
	font-weight: bold;
}
.storename{
	margin-top: 15rpx;
	color: #9194ae;
	font-size: small;
}

.goodsitem{
	display: flex;
	flex-direction: row;
	
}
.goods{
	margin-top:15rpx ;
	background-color: #ffffff;
	border-radius: 25px;
	flex-direction: row;
	margin-left: 25rpx;
	margin-right: 25rpx;
}
</style>
