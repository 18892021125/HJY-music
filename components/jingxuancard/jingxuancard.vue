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
						{maintt:"国风民乐！太好听了！",subtt:"声色犬马",src:"../../static/img/jx/jx1.png",islike:1},
						{maintt:"琵琶爱好者不要错过~",subtt:"努力练琴的小雅",src:"../../static/img/jx/jx3.png",islike:0},
						{maintt:"印象国乐·大典",subtt:"风铃筝语",src:"../../static/img/jx/jx2.png",islike:0},
						{maintt:"还原唐乐！震撼！",subtt:"紫山曼居的二胡",src:"../../static/img/jx/jx4.png",islike:0},
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
	
	float: left;
	
	border-radius: 45rpx;
}
.jxinfo{
	
	width: 350rpx;
	
	flex-direction: row;
}
	
.bottominfo{
	margin-left: 15rpx;
	display: flex;
	flex-direction:row;
	
	
}
.textinfo{
	text-align: left;

	margin-left: 20rpx;
}
.maintt{
	font-size: 25rpx;
	color: #000000;
	
}
.subtt{
	font-size: 10rpx;
	color: #d0b06a;
}
.imginfo{
	height: 400rpx;
	width: 300rpx;
}
	
.likeinfo{

	float: right;
	margin-left: auto;
	margin-right: 23rpx;
}
.likeimage{
	margin-top: 30rpx;
	width: 30rpx;
	height: 30rpx;
	float:right;
}

</style>
