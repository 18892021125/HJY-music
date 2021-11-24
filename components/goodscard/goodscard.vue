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
					<font class="type">$：</font>
					<font >{{val.cost}}</font>
					<font>元</font>
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
						{name:"木管乐器1",storename:"Woodwind instrument1",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器2",storename:"Woodwind instrument2",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器3",storename:"Woodwind instrument3",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						{name:"木管乐器4",storename:"Woodwind instrument4",src:"../../static/img/muguan.png",cost:999},
						
					]
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.textinfo{
	margin-left: 20px;
	display: flex;
	flex-direction: column;
}
.costcard{
	background-color: #ffe8e6;
	display: inline;
	padding:15rpx ;
	border-radius: 20rpx;
	margin-top: auto;
	margin-bottom: auto;
	margin-left: auto;
	margin-right: 19rpx;
	float: right;
	

}
.type{
	color: #FF6034;
	face:"黑体";
}
.name{
	color: #0000ff !important;
	font-weight: bold;
}
.storename{
	color: #5500ff;
	font-size: small;
}

.goodsitem{
	display: flex;
	flex-direction: row;
	
}
.goods{
	margin-top:15rpx ;
	background-color: #fffcf3;
	border-radius: 25px;
	flex-direction: row;
	margin-left: 25rpx;
	margin-right: 25rpx;
}
</style>
