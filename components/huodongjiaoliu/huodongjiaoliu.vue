<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="活动交流" backgroundColor="#f8eee2" ></uni-nav-bar>
		<view v-for="(val,index) in yuepilist.list" class="jingxuanitem" @click="goUrl('/components/huodongxiangqing/huodongxiangqing')">
			<view v-if="val.name" class="jxtitle">{{val.name}}</view>
			<image v-if="val.src" class="jximage" :src="val.src"></image>
			<view class="more">了解更多</view>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniNavBar,
		},
		data() {
			return {
				yuepilist:{
					title:"活动信息",
					list:[
						{name:"1元秒杀",src:"../../static/img/huodong1.png"},
						{name:"集贤鼓乐VS大唐芙蓉园",src:"../../static/img/huodong2.png"},
						{name:"穿唐服，学唐乐",src:"../../static/img/huodong3.png"},
						{name:"1元秒杀",src:"../../static/img/huodong1.png"},
						{name:"集贤鼓乐VS大唐芙蓉园",src:"../../static/img/huodong2.png"},
					
					]
				},
			}
		},
		methods: {
			back() {
				uni.navigateBack({
					delta: 1
				})
			},
			goUrl : function (str){
				uni.navigateTo({
					url: str
				});
			},
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #f8eee2;
	}
.jingxuanitem{

	margin:25rpx;
	margin-top:30rpx;
	margin-bottom: 30rpx;
}
.jxtitle{
	
	margin-bottom: 30rpx;
	letter-spacing: 6rpx;
	
	font-size: 40rpx;
}
.jximage{
	width: 700rpx;
	height: 300rpx;
}
.more{

	float: right;
	margin-right: 30rpx;
	margin-top: 15rpx;
	font-size: 30rpx;
	color: #98989a;
}
</style>
