<template>
	<view class="indexinall">
		<view v-for="(val,index) in dtinfo.list" class="index" >
			<view class="posterinfo">
				<image v-if="val.src" class="posterimg" :src="val.src"></image>
				<view class="textinfo">
					<font v-if="val.postername" class="postname">{{val.postername}}</font>
					<br>
					<font v-if="val.subtitile" class="likeinfo">{{val.subtitile}}</font>
				</view>
				
			</view>
			<p v-if="val.title" class="title">{{val.title}}</p>
			
			<p v-if="val.content" class="content">{{val.content}}</p>
			<view class="imageinfo">
				<image v-if="val.src1" class="imageitem" :src="val.src1"></image>
				<image v-if="val.src2" class="imageitem" :src="val.src2"></image>
				<image v-if="val.src3" class="imageitem" :src="val.src3"></image>
				
			</view>
			<view class="moreaction">
				<image class="redheart" src="../../static/img/jx/likefill.png"></image>
				<p v-if="val.likenum">{{val.likenum}}</p>
				<image class="comment" src="../../static/img/explore-selected.png"></image>
				<p v-if="val.commentnum">{{val.commentnum}}</p>
				<image class="moreinfo" src="../../static/img/user-selected.png"></image>
			</view>
			<view class="line"></view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			dtinfo:{
				title:"动态信息",
				list:[
					{postername:"木管乐器1",subtitile:"Woodwind instrument1",src:"../../static/img/follow1.png",title:"宝藏音乐分享！",like:1,commentnum:356,likenum:359,src1:"../../static/img/goods/goods3.png",src2:"../../static/img/goods/goods3.png",src3:"../../static/img/goods/goods3.png",content:"大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的"},
					{postername:"木管乐器1",subtitile:"Woodwind instrument1",src:"../../static/img/follow2.png",title:"宝藏音乐分享！",like:1,commentnum:356,likenum:359,src1:"../../static/img/goods/goods3.png",src2:"../../static/img/goods/goods3.png",src3:"../../static/img/goods/goods3.png",content:"大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的"},
					{postername:"木管乐器1",subtitile:"Woodwind instrument1",src:"../../static/img/follow2.png",title:"宝藏音乐分享！",like:1,commentnum:356,likenum:359,src1:"../../static/img/goods/goods3.png",src2:"../../static/img/goods/goods3.png",src3:"../../static/img/goods/goods3.png",content:"大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的大受打击啊菩萨的就怕是假的帕金斯的"},
					
				]
			},
			}
		},
		
		
			
		
		methods: {
			
		}
	}
</script>

<style lang="scss"> 
.posterinfo{
	display: flex;
	flex-direction: row;
}
.posterimg{
	margin-top: 30rpx;
	width: 80rpx;
	height: 80rpx;
}
.textinfo{
	margin-left: 20rpx;
	margin-top: 30rpx;
}
	
.likeinfo{
	font-size: 15rpx;
	color: #7c7c7c;
	letter-spacing: 2rpx;
}
.indexinall{
	margin-top: 30rpx;
	background-color: #FFFFFF;
	border-top-left-radius: 45rpx;
	border-top-right-radius: 45rpx;
}
.index{
	
	
	padding-left: 40rpx;
	padding-right: 40rpx;
	width: auto;
}
.title{
	padding-top: 10rpx;
	color: #000000;
	font-weight: bold;
	line-height: 80rpx;
	font-size: 30rpx;
}
	
.postname{
	font-weight: bold;
	font-size: 29rpx;

}
	
.content{
	font-size: 28rpx;
	line-height: 45rpx;
}
	
.imageinfo{
	margin-top: 20rpx;
	padding-bottom: 20rpx;
	display:flex;
}
.imageitem{
	margin-left: 5rpx;
	margin-right: 5rpx;
	flex:1;
	width: 210rpx;
	height: 210rpx;
}
.moreaction{
	display: flex;
	flex-direction: row;
	margin-top: 20rpx;
	padding-bottom: 20rpx;
}
.redheart{
	margin-right: 20rpx;
	width: 40rpx;
	height: 30rpx;
}
.moreinfo{
	float: right;
	margin-left: auto;
	width: 30rpx;
	height: 30rpx;
}
.comment{
	margin-right: 20rpx;
	margin-left: 160rpx;
	width: 30rpx;
	height: 30rpx;
}
.line{
		position: relative;
		
		margin-top:30rpx;
		
		margin-left: 25rpx;
		margin-right: 25rpx;

		height: 1px;
		background-color: rgba(202, 203, 196, 1.0);
		text-align: center;
		font-size: 16px;
	
		

	
		
	}
</style>
