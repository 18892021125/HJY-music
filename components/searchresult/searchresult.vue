<template>
	<view>
		<view class="buttonindex">
			<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
			<view class="uni-padding-wrap uni-common-mt">
				<uni-segmented-control :current="current" :values="items" :style-type="styleType"
					:active-color="activeColor" @clickItem="onClickItem" />
			</view>
		</view>
		<view class="content">
			<view v-if="current === 0"><yuepu></yuepu></view>
			<view v-if="current === 1"><banzou></banzou></view>
			<view v-if="current === 2"><yueshou></yueshou></view>
		</view>
	</view>
</template>

<script>
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import yuepu from '../../components/yuepu/yuepu';
	import banzou from '../../components/banzou/banzou';
	import yueshou from '../../components/yueshou/yueshou'
	export default {
		components: {uniSegmentedControl,
					yuepu,
					banzou,
					yueshou,
		},
		data() {
			return {
				items: ['乐谱','伴奏','乐手'],
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
		}
	}
</script>

<style>
		
	page{
		background-color: #f8eee2;
	}
.buttonindex{
	
}
</style>
