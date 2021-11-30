<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="课程试看" backgroundColor="#f8eee2" ></uni-nav-bar>
		
		<image class="mainimg" src="../../static/img/kechengxiangqingzhutu.png"></image>
		<view class="kechengjieshao">
			<view class="cptname">第一节：乐社简介</view>
			<view class="info">何家营鼓乐(西安何家营鼓乐社)是西安市何家营村的独特民间鼓乐，据学者考证，乐社历史与隋唐乐舞有渊源。
</view>
			<view class="info">1952年至1953年，杨荫浏，简其华等中央音乐学院民族音乐研究所众人，与陕西音乐工作者李石根等人采访西安鼓乐并编写《陕西的鼓乐与铜器社》调查报告。之后西安何家营鼓乐开始受到学术界的关注。
</view>
			<view class="info">2009年，何家营鼓乐被联合国教科文组织列入“人类口头和非物质文化遗产名录”。何家营鼓乐源于隋唐，历经四代，宋，元，明，清，依笛为首，群笙协和，属于西安鼓乐道、僧、俗、三大流派之一的俗派。</view>
			<view class="line"></view>
			<view  v-for="(val,index) in kecheng.list">
				<view v-if="val.name" class="xiaojieneirong">
					<view class="xiaojiename">{{val.name}}</view>
					<image class="playicon" src="../../static/img/music/playimg.png"></image>
				</view>
				<view class="line"></view>
			</view>
		</view >
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
				kecheng:{
					title:"课程信息",
					list:[
						
						{name:"第二节：鼓乐的音乐之美"},
						{name:"第三节：掌握鼓乐技法"},
						{name:"第四节：音准的控制"},
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
.mainimg{
	margin-left: auto;
	margin-right: auto;
	display: flex;
	border-radius: 40rpx;
	width: 90%;
	margin-top: 20rpx;
	
}
.kechengjieshao{
	margin-top: 50rpx;
	margin-left: 40rpx;
	margin-right: 40rpx;
	padding-left: 20rpx;
	padding-right: 20rpx;
	background-color: #ffffff;
	border-radius: 40rpx;
	position: absolute;
	height: 100%;
}
.cptname{
	margin-bottom: 40rpx;
	padding-top: 40rpx;
	font-size: 35rpx;
	
}
.info{
	text-indent:20px;
	color: #98989a;
	letter-spacing: 2rpx;
}
.playicon{
	width: 80rpx;
	height: 80rpx;
	float: right;
	margin-left: auto;
	margin-right: 30rpx;
}
.xiaojieneirong{
	display: flex;
	flex-direction: row;
}
.xiaojiename{
	margin: 20rpx;
	font-size: 35rpx;
	margin-left: 5rpx;
}
.line{
		position: relative;
		
		margin-top:37rpx;
		
		margin-left: 15rpx;
		margin-right: 15rpx;
		margin-bottom: 35rpx;
		height: 1px;
		background-color: rgba(239, 239, 243, 1.0);
		text-align: center;
		font-size: 16px;
		color: rgba(239, 239, 243, 1.0);
		

	
		
	}
</style>
