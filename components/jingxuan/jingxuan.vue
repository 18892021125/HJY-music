<template>
	<view class="index">
	<br>
	
	<br>
	
	<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
	<font class="guesslike">猜你喜欢</font>
	
	<jingxuangundong></jingxuangundong>
	<view class="uni-padding-wrap uni-common-mt">
		<uni-segmented-control :current="current" :values="items" :style-type="styleType"
			:active-color="activeColor" @clickItem="onClickItem" />
	</view>
	<view class="content">
		<view v-if="current === 0"><text class="content-text"><jingxuancard></jingxuancard></text></view>
		<view v-if="current === 1"><text class="content-text">选项卡2的内容</text></view>
		<view v-if="current === 2"><text class="content-text">选项卡3的内容</text></view>
	</view>
	
	</view>
</template>

<script>
	import jingxuangundong from '@/components/jingxuangundong/jingxuangundong';
	import {ref} from '../../vue.js';
	import jiaoliu from '@/components/jingxuan/jiaoliu';
	import yuanchuang from '@/components/jingxuan/yuanchuang';
	import yanchu from '@/components/jingxuan/yanchu';
	import tuijian from '@/components/jingxuan/tuijian';
	import jingxuancard from '@/components/jingxuancard/jingxuancard';
	import {uniSegmentedControl} from '@dcloudio/uni-ui'
	export default {
		 components: {uniSegmentedControl,
			jingxuancard,
			jingxuangundong,
		 },
		data() {
			return {
			items: ['推荐', '交流', '演出','原创'],
			current: 0,
			colorIndex: 0,
			activeColor: '#ff7361',
			styleType: 'text',
			}
		},
		setup() {
		    const active = ref(0);
		    return { active };
		  },
		methods: {
			onClickItem(e) {
							if (this.current !== e.currentIndex) {
								this.current = e.currentIndex
							}
						},
						styleChange(e) {
							if (this.styleType !== e.detail.value) {
								this.styleType = e.detail.value
							}
						},
						colorChange(e) {
							if (this.styleType !== e.detail.value) {
								console.log(e.detail.value);
								this.activeColor = e.detail.value
							}
						}
		
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #F8EEE2;
	}
		
	
	.uni-common-mt {
			margin-top: 30px;
			text-align: center;
		}
	
	.uni-padding-wrap {
		// width: 750rpx;
		padding: 0px 30px;
	}
	.content {
			
		}
</style>
