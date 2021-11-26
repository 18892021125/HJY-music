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
			
		</view>
	</view>
</template>

<script>
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import yuepu from '../../components/yuepu/yuepu';
	export default {
		components: {uniSegmentedControl,
					yuepu,
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
			
		}
	}
</script>

<style>
		
	page{
		background-color: #55aaff;
	}
.buttonindex{
	
}
</style>
