<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="谱曲收藏" backgroundColor="#f8eee2" ></uni-nav-bar>
		<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="content">
			<view v-if="current === 0"><shoucangpuquitem></shoucangpuquitem></view>
			<view v-if="current === 1"><shoucangpujiitem></shoucangpujiitem></view>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniSearchBar} from '@dcloudio/uni-ui';
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import shoucangpuquitem from '../../components/shoucangpuquitem/shoucangpuquitem';
	import shoucangpujiitem from '../../components/shoucangpujiitem/shoucangpujiitem';
	export default {
		components:{
			uniSearchBar,
			uniNavBar,
			uniSegmentedControl,
			shoucangpuquitem,
			shoucangpujiitem,
		},
		data() {
			return {
				items: ['谱曲','谱集'],
				current: 0,
				colorIndex: 0,
				activeColor: '#ff7361',
				styleType: 'text',
				
			}
		},
		methods: {
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
			back() {
				uni.navigateBack({
					delta: 1
				})
			},
		}
	}
</script>

<style lang="scss">
	.content{
		background-color: #ffffff;
		border-top-left-radius: 55rpx ;
		border-top-right-radius:55rpx;
		padding-top: 25rpx;
		margin-top: 50rpx;
		height:100%;
		width: 100%;
		position:absolute; 
	}
	page{
		background-color: #f8eee2;
		}

</style>
