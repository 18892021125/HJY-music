<template>
	<view class="jxcardmain">
		<view class="jxcard" v-for="(val,index) in jxcard.list" :key="index" @tap="goUrl('./pages/user/user')">
			<view class="jxinfo">
				<image  v-if="val.src" :src="val.src" style="width: 300rpx;height: 400rpx;">
				<view class="bottominfo">
					<view class="textinfo">
					<font v-if="val.maintt" class="maintt" >{{val.maintt}}</font>
					<br>
					<font v-if="val.subtt" class="subtt">{{val.subtt}}</font>
					</view>
					<view class="likeinfo">
						<image v-if="val.islike == 0" class="likeimage" src="../../static/img/jx/likeempty.png"></image>
						<image v-if="val.islike == 1" class="likeimage" src="../../static/img/jx/likefill.png"></image>
					</view>
				</view>
				
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				jxcard:{
					title:"精选信息",
					list:[
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx1.png",islike:1},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx2.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx3.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx1.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx3.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx4.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx1.png",islike:0},
						
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx3.png",islike:0},
						{maintt:"木管乐器1",subtt:"Woodwind instrument1",src:"../../static/img/jx/jx2.png",islike:0},
						
						
					
					]
				},
			}
		},
		methods: {
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
			styleChange(e) {
				if (this.styleType !== e.detail.value) {
					this.styleType = e.detail.value
				}
			},
			colorChange(e) {
				if (this.styleType !== e.detail.value) {
					console.log(e.detail.value);
					this.activeColor = e.detail.value
				}
			}
		}
	}
</script>

<style lang="scss">
.jxcardmain{
	position: absolute;
	background-color: #F8EEE2;
}
.jxcard{
	padding-left: 15rpx;
	margin-top: 15rpx;
	text-align: center;
	width: min-content;
	float: left;
}
.jxinfo{

	width: 350rpx;
	
	flex-direction: row;
}
	
.bottominfo{
	margin-left: 15rpx;
	display: inline-flex;
	flex-direction:row;
	
	
}
.textinfo{
	text-align: left;
}
.maintt{
	font-size: 10rpx;
	color: #0000FF;
	font-weight: bold;
}
.subtt{
	font-size: 10rpx;
	color: #07C160;
}
.imginfo{
	height: 400rpx;
	width: 300rpx;
}
	
.likeinfo{

	text-align: center;
	margin-left: 30rpx;
}
.likeimage{
	margin-top: 30rpx;
	width: 30rpx;
	height: 30rpx;
	float:right;
}

</style>
