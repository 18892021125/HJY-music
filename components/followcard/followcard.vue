<template>
	<view >
		<uni-nav-bar left-icon="back" @clickLeft="back" title="关注列表" backgroundColor="#f8eee2" ></uni-nav-bar>
		<uni-search-bar placeholder="搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		<view class="followuser" v-for="(val,index) in follows.list" :key="index" @tap="goUrl('./pages/user/user')">
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
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniSearchBar} from '@dcloudio/uni-ui';
	
	export default {
		components:{
			uniNavBar,
		},
		data() {
			return {
			follows:{
				title:"关注列表",
				list:[
					{name:"user1",sign:"test sign",src:"../../static/img/follow1.png"},
					{name:"user2",sign:"test sign128888888",src:"../../static/img/follow2.png"},
					{name:"user3",sign:"test sign23",src:"../../static/img/follow1.png"},
					{name:"user4",sign:"test sign34",src:"../../static/img/follow2.png"},
					{name:"user5",sign:"test sign45",src:"../../static/img/follow1.png"},
					{name:"user6",sign:"test sign56",src:"../../static/img/follow2.png"},
					
					{name:"user7",sign:"test sign67",src:"../../static/img/follow1.png"},
					{name:"user8",sign:"test sign78",src:"../../static/img/follow2.png"},
					{name:"user9",sign:"test sign89",src:"../../static/img/follow1.png"},
					
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
		}
	}
</script>

<style lang="scss"> 
page{
	background-color: #f8eee2;
}
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
	background-color: #FFFFFF;
	border-radius: 25px;
	flex-direction: row;
	height: 160rpx;
}
</style>