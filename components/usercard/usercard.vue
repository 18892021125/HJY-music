<template>
	<view >
		<view class="followuser" v-for="(val,index) in prodata.list" :key="index" @tap="goUrl('./pages/user/user')">
			<view class="followitem">
				<image v-if="val.src" :src="val.src" style="width: 70px; height: 70px; margin-top: 15rpx;margin-left: 15rpx; ">
				<view class="followinfo">
					<br>
					<font v-if="val.name" class="name">{{val.name}}</font>
				    
					<font v-if="val.sign" class="sign">{{val.sign}}</font>
					
				</view>
				<view class="moreinfoicon" >
					<uni-icons custom-prefix="iconfont" type="icon-moreinfo" size="25" @click="playmusic" ></uni-icons>
				</view>		
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			prodata: {
				type: String,
				default: []
			},
			
		},
		data() {
			return {
			
			}
		},
		
		
			
		
		methods: {
			
		}
	}
</script>

<style lang="scss"> 
.followinfo{
	margin-left: 20px;
	display: flex;
	flex-direction: column;
}
.moreinfoicon{
	display: inline;
	margin-top: auto;
	margin-bottom: auto;
	margin-left: auto;
	float: right;
	

}
.type{
	color: #FF6034;
	face:"黑体";
}
.name{
	color: #000000;
	font-weight: bold;
}
.sign{
	color: #969799;
	font-size: small;
}

.followitem{
	display: flex;
	flex-direction: row;
	
}
.followuser{
	margin-left: 15rpx;
	margin-right:15rpx ;
	margin-top:15rpx ;
	background-color: #fffcf3;
	border-radius: 25px;
	flex-direction: row;
	height: 160rpx;
}
</style>
