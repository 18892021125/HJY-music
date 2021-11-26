<template>
	<view class="index">

	
	<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
	<view class="guesslike">
	<font>猜你喜欢</font>
	</view>

	<jingxuangundong></jingxuangundong>
	<view class="uni-padding-wrap uni-common-mt">
		<uni-segmented-control :current="current" :values="items" :style-type="styleType"
			:active-color="activeColor" @clickItem="onClickItem" />
	</view>
	<view class="content">
		<view v-if="current === 0"><jingxuancard></jingxuancard></view>
		
	</view>

	

	
	</view>
</template>

<script>
	import jingxuangundong from '@/components/jingxuangundong/jingxuangundong';
	import {ref} from '../../vue.js';
	

	import jingxuancard from '@/components/jingxuancard/jingxuancard';
	import {uniSegmentedControl} from '@dcloudio/uni-ui'
	export default {
		 components: {uniSegmentedControl,
			jingxuancard,
			jingxuangundong,
		 },
		data() {
			return {
			items: ['推荐'],
			current: 0,
			colorIndex: 0,
			activeColor: '#ff7361',
			styleType: 'text',
		
		}
	}
	}
</script>

<style lang="scss">
	.index{
		
		margin-top: 65rpx;
		background-color:#ffe8e6;
		
	}
	.guesslike{
		background-color: #ffe8e6;
		color: #000000;
		font-size: 40rpx;
		margin-left: 45rpx;
		height: 10rpx;
	}
	
		
	
	.uni-common-mt {
	
			text-align: center;
		}
	
	.uni-padding-wrap {
		// width: 750rpx;
		padding: 0px 30px;
		background-color: #ffe8e6;
	}
	.content {
			
		background-color: #ffe8e6;

		
	}

	
	
	
	.uni-padding-wrap {
		// width: 750rpx;
		
	}
	
	.content {
		
		
	}
	
	.content-text {
		
	}
		
	

</style>
