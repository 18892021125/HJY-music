<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="离线缓存" backgroundColor="#f8eee2" ></uni-nav-bar>
		<uni-search-bar placeholder="缓存搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="content">
			<view v-if="current === 0"></view>
			<view v-if="current === 1"><xiazaizhong></xiazaizhong></view>
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
				items: ['已下载','下载中'],
				current: 1,
				colorIndex: 0,
				activeColor: '#ff7361',
				styleType: 'text',
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
	margin-top:40rpx;
	padding-top:40rpx;
	background-color: #FFFFFF;
	height: 100%;
	width: 100%;
	position: absolute;
	border-top-left-radius: 55rpx;
	border-top-right-radius: 55rpx;
}
</style>
