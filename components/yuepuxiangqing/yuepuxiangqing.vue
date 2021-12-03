<template>
	<view>
		<view class="buttonindex">
			<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
			<view class="uni-padding-wrap uni-common-mt">
				<uni-segmented-control :current="current" :values="items" :style-type="styleType"
					:active-color="activeColor" @clickItem="onClickItem" />
			</view>
		</view>
		<view v-if="current === 0">
			<view class="yuepiinfo">
				<image class="yuepu" src="../../static/img/music/yuepu1.png"> </image>
				<uni-fab ref="fab" :pattern="pattern" :content="content" :horizontal="horizontal" :vertical="vertical"
					:direction="direction" @trigger="trigger"/>
			</view>
		</view>
		<view v-if="current === 1">
			<view class="yuepiinfo">
				<image class="yuepu" src="../../static/img/music/yuepu1.png"> </image>
				
				<view  class="playcard">
					<image class="musicimg" src="../../static/img/music/music1.png"></image>
					<view class="musicinfo">
						<view class="musicname">平调曲破</view>
						<view class="musician">未知音乐人</view>
					</view>
					<image class="playicon" src="../../static/img/music/playimg.png"></image>
				</view>
				<view  class="tiaosuoption">
				<view class="actionitem">
					<image class="actionicon1" src="../../static/img/biandiaojia.png"></image>
					<view class="actionname">变调夹</view>
				</view>
				<view class="actionitem">
					<image class="actionicon2" src="../../static/img/yingui.png"></image>
					<view class="actionname">音轨</view>
				</view>
				<view class="actionitem">
					<image class="actionicon3" src="../../static/img/mute.png"></image>
					<view class="actionname">静音</view>
				</view>
				<view class="actionitem">
					<image class="actionicon4" src="../../static/img/beisu.png"></image>
					<view class="actionname">倍速</view>
				</view>
				<view class="actionitem">
					<view class="actionicon5">AA</view>
					<view class="actionname">显示</view>
				</view>
				<view class="actionitem" >
					<image class="actionicon6" src="../../static/img/moreaction.png" @click="showDrawer"></image>
					<view class="actionname">更多</view>
				</view>
			</view>
			</view>
		</view>
		<view v-if="current === 2">
			
		</view>
		
		<uni-drawer ref="showRight" mode="right" :mask-click="true" width="300">
			<scroll-view style="height: 100%;" scroll-y="true">
				<tiaoyingengduo></tiaoyingengduo>
				
			</scroll-view>
		</uni-drawer>
	</view>
</template>

<script>
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import {uniFab} from '@dcloudio/uni-ui';
	import {uniDrawer} from '@dcloudio/uni-ui';
	import tiaoyingengduo from '../../components/tiaoyingengduo/tiaoyingengduo';
	export default {
		components: {
			uniSegmentedControl,
			uniFab,
			uniDrawer,
			tiaoyingengduo,
		},
		data() {
			
			return {
				items: ['乐谱','伴奏','乐手'],
				current: 0,
				colorIndex: 0,
				activeColor: '#ff7361',
				styleType: 'text',
				horizontal: 'right',
				vertical: 'bottom',
				direction: 'vertical',
				istiaosu:false,
				content: [{
					iconPath: '../../static/img/jx/likeempty.png',
					selectedIconPath: '../../static/img/redheart.png',
					text: '收藏',
					active: false
				},
				{
					iconPath: '../../static/img/tiaosu.png',
					selectedIconPath: '../../static/img/tiaosu.png',
					text: '调速',
					active: false
				},
				],
				pattern: {
					color: '#ffffff',
					backgroundColor: '#e4b4aa',
					selectedColor: '#ff7361',
					buttonColor: '#f8eee2',
					iconColor: '#fff'
				},
			}
		},
		methods: {
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
			fabClick() {
				uni.showToast({
				
				})
				
			},
			trigger(e) {
				console.log(e)
				this.content[e.index].active = !e.item.active
			
				this.istiaosu=true;
			},
			showDrawer() {
							this.$refs.showRight.open();
						},
			closeDrawer() {
			                this.$refs.showRight.close();
			            }

		}
	}
</script>

<style lang="scss">
page{
	background-color: #f8eee2;
}
.playcard{
	display: flex;
	flex-direction: row;
	
	
	padding-left: 40rpx;
	padding-right: 40rpx;
	
	background-color: #e4b4aa;
	position: fixed;
	left: 0;
	right: 0;
	/* #ifdef H5 */
	left: var(--window-left);
	right: var(--window-right);
	/* #endif */
	bottom: 100rpx;
	width: 100%;
	margin-left: auto;
	margin-right: auto;
	padding-bottom: 50rpx;
	padding-top: 30rpx;
	
	border-top-left-radius: 35rpx;
	border-top-right-radius: 35rpx;
}
.musicinfo{
	margin-left: 20rpx;
	
}
.musicname{
	margin:5rpx;
	font-size: 40rpx;
	color:#FFFFFF;
	letter-spacing: 8rpx;
}
.musician{
	margin:5rpx;
	color: #FFFFFF;
	letter-spacing: 5rpx;
}
.playicon{
	width: 80rpx;
	height: 80rpx;
	float: right;
	margin-left: auto;
}

.musicimg{
	width: 100rpx;
	height: 100rpx;
}
.yuepiinfo{
	margin-top: 50rpx;
	padding-top: 90rpx;
	background-color: #FFFFFF;
	border-top-left-radius: 45rpx;
	border-top-right-radius: 45rpx;
	height: 100%;
	width: 100%;
	position: absolute;
}
.yuepu{
	display: flex;
	margin-left: auto;
	margin-right: auto;
	height: 1000rpx;
	width: 90%;
}
	
.tiaosuoption{
	background-color: #ffffff;
	padding-top: 30rpx;
	display: flex;
	flex-direction: row;
	position: fixed;
	left: 0;
	right: 0;
	/* #ifdef H5 */
	left: var(--window-left);
	right: var(--window-right);
	/* #endif */
	bottom: 0;
	width: 100%;
	margin-left: auto;
	margin-right: auto;
	padding-bottom: 20rpx;
	border-top-left-radius: 35rpx;
	border-top-right-radius: 35rpx;
}
.actionitem{
	margin-left: auto;
	margin-right: auto;
	text-align: center;
}
.actionicon1{
	width: 45rpx;
	height: 39rpx;
	
}
.actionicon2{
	width: 40rpx;
	height: 39rpx;
	
}
.actionicon3{
	width:41rpx;
	height: 39rpx;
	
}
.actionicon4{
	width: 50rpx;
	height: 39rpx;
	
	
}
.actionicon5{
	font-size: 37rpx;
	
}
.actionicon6{
	width: 60rpx;
	height: 39rpx;
	
}

</style>
