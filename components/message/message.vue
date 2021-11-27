<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="消息" backgroundColor="#f8eee2" ></uni-nav-bar>
		<uni-search-bar placeholder="搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="content">
			<view v-if="current === 0">
				<view class="messagelist">
					<view v-for="(val,index) in messagelist.list">
						<view class="messageitem">
							<image v-if="val.src" class="headimg" :src="val.src"></image>
							<view class="textinfo">
								<view v-if="val.name" class="name">
									{{val.name}}
								</view>
								<view v-if="val.content" class="messageinfo">
									{{val.content}}
								</view>
							</view>
								
							<view v-if="val.time" class="time">
								{{val.time}}
							</view>
						</view>
						<view class="line"></view>
					</view>
					
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniNavBar,
			uniSegmentedControl,
		},
		data() {
			return {
				items: ['已读','未读'],
				current: 0,
				colorIndex: 0,
				activeColor: '#ff7361',
				styleType: 'text',
				messagelist:{
					title:"消息信息",
					list:[
						{name:"菠萝爱音乐",content:"下午七点记得排练！",time:"13:01",src:"../../static/img/message1.png"},
						{name:"禅 语",content:"尊敬的会员，鼓乐设期待你的加入！",time:"14:20",src:"../../static/img/message2.png"},
						
					
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
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
		}
	}
</script>

<style lang="scss">
		
	page{
		background-color: #f8eee2;
	}
		
	.content{
		margin-top: 40rpx;
		background-color: #ffffff;
		border-top-left-radius: 45rpx;
		border-top-right-radius: 45rpx;
		height:100%;
		width: 100%;
		position:absolute; 
	}
	.textinfo{
		display: flex;
		flex-direction: column;
		margin-left: 25rpx;
	}
	.name{
		letter-spacing: 4rpx;
		
		font-size: 32rpx;
	}
	.messageinfo{
		margin-top:20rpx;
		color: #98989a;
		font-size: 25rpx;
	}
	.messageitem{
		margin-left: 35rpx;
		margin-right: 35rpx;
		padding-top:30rpx;
		display: flex;
		flex-direction: row;
		
	}
	.headimg{
		margin-left: 20rpx;
		height: 100rpx;
		width: 100rpx;
	}
	.line{
			position: relative;
			margin-top:30rpx;
			margin-left: 55rpx;
			margin-right: 55rpx;
			height: 1px;
			background-color: rgba(231, 231, 237, 1.0);
			text-align: center;
			font-size: 16px;
		}
	.time{
		text-align:center;
		display: flex;
		float: right;
		margin-left: auto;
		color: #98989a;
		letter-spacing: 2rpx;
		font-size: 20rpx;
		margin-top: 30rpx;
		margin-right: 25rpx;
	}
</style>
