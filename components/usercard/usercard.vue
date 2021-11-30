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
				<image class="comment" src="../../static/img/pinglundongtai.png"></image>
				<p v-if="val.commentnum">{{val.commentnum}}</p>
				<image class="moreinfo" src="../../static/img/sangedian.png"></image>
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
					{postername:"音乐自律一点",subtitile:"2万人赞了他",src:"../../static/img/dongtaitouxiang.png",title:"宝藏音乐分享！",like:1,commentnum:79,likenum:342,src1:"../../static/img/dongtai1.png",src2:"../../static/img/dongtai2.png",src3:"../../static/img/dongtai3.png",content:"在听音乐这件事上，我是不专业的，所以在发现有无数好听音乐的—更确切地说，是有无数承载着好听的音乐的专辑的—Putumayo的时候，发现了宝藏。接下来除了自己听，自然是要将其推而广之，惠及各位好友。"},
					{postername:"西安音乐",subtitile:"5万人赞了他",src:"../../static/img/dongtaitouxiang2.png",title:"大唐芙蓉园|来西安感受盛唐宫廷音乐剧",like:1,commentnum:356,likenum:359,src1:"../../static/img/dongtai4.png",src2:"../../static/img/dongtai5.png",src3:"../../static/img/dongtai6.png",content:"故事讲述唐长安一天赋少年历经考验成长为一代传奇鼓师，并成为玄宗鼓乐知音，在千秋寿宴上大放异彩。观众作为参与梨园考试的乐工，带着自己的角色参与到剧情中，于是，“口传心授”的真谛在少年梨园学艺过程中，以音乐表演与互动的方式全方位传递给观众。"},
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
	margin-top: 15rpx;
	margin-right: 15rpx;
	height: 10rpx;
	width: 35rpx;
	
}
.comment{
	margin-right: 20rpx;
	margin-left: 100rpx;
	width: 30rpx;
	height: 30rpx;
}
.line{
		position: relative;
		
		margin-top:30rpx;
		
		margin-left: 15rpx;
		margin-right: 15rpx;

		height: 1px;
		background-color: rgba(231, 231, 237, 1.0);
		text-align: center;
		font-size: 16px;
	
		

	
		
	}
</style>
