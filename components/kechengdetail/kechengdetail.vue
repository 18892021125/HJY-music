<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="课程" backgroundColor="#f8eee2" ></uni-nav-bar>
		<uni-search-bar placeholder="课程搜索" :radius="100"  @confirm="goUrl('/components/searchresult/searchresult')"></uni-search-bar>
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="content">
			<view v-if="current === 0"><kechengjingxuan></kechengjingxuan></view>
			
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniSearchBar} from '@dcloudio/uni-ui';
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import kechengjingxuan from '@/components/kechengjingxuan/kechengjingxuan'
	export default {
		components:{
			uniNavBar,
			uniSearchBar,
			uniSegmentedControl,
		},
		data() {
			return {
				items: ['精选','木管音乐','铜管音乐','鼓乐'],
				current: 0,
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
		}
	}
</script>

<style lang="scss">
page{
	background-color: #f8eee2;
}
</style>
