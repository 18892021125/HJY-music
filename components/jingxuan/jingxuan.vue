<template>
	<view class="index">
	<br>
	
	<br>
	
	<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
	<font class="guesslike">猜你喜欢</font>
	
<<<<<<< HEAD
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
=======
	
	<view class="uni-padding-wrap uni-common-mt">
		<uni-segmented-control :current="current" :values="items" style-type="text"
				:active-color="activeColor" @clickItem="onClickItem" />
	</view>
	<view class="content">
		<view v-if="current === 0">
			<tuijiancard></tuijiancard>
		</view>
		<view v-if="current === 1"><text class="content-text">选项卡2的内容</text></view>
		<view v-if="current === 2"><text class="content-text">选项卡3的内容</text></view>
	</view>
	
>>>>>>> 581906dc5a75fb04c786292dec069b0404f87f7e
	
	</view>
</template>

<script>
	import jingxuangundong from '@/components/jingxuangundong/jingxuangundong';
	import {ref} from '../../vue.js';
	import jiaoliu from '@/components/jingxuan/jiaoliu';
	import yuanchuang from '@/components/jingxuan/yuanchuang';
	import yanchu from '@/components/jingxuan/yanchu';
	import tuijian from '@/components/jingxuan/tuijian';
<<<<<<< HEAD
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
=======
	import tjcard from '@/components/tuijiancard/tuijiancard';
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import tuijiancard from '@/components/tuijiancard/tuijiancard';
	export default {
		components: {uniSegmentedControl},
		data() {
			return {
			items: ['精选', '交流','演出' ,'原创'],
			styles: [{
					value: 'button',
					text: '按钮',
					checked: true
				},
				{
					value: 'text',
					text: '文字'
				}
			],
			colors: ['#007aff', '#4cd964', '#dd524d'],
			current: 0,
			colorIndex: 1,
			activeColor: '#007aff',
			styleType: 't'
>>>>>>> 581906dc5a75fb04c786292dec069b0404f87f7e
			}
		},
		setup() {
		    const active = ref(0);
		    return { active };
		  },
		methods: {
			onClickItem(e) {
<<<<<<< HEAD
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
=======
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
>>>>>>> 581906dc5a75fb04c786292dec069b0404f87f7e
		
		}
	}
</script>

<style lang="scss">
	page{
<<<<<<< HEAD
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
=======
		background-color: #ff00ff;
	}
	
	.example-body {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: row;
		padding: 0;
	}
	
	.uni-common-mt {
		margin-top: 30px;
	}
	
	.uni-padding-wrap {
		// width: 750rpx;
		padding: 0px 30px;
	}
	
	.content {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		justify-content: center;
		align-items: center;
		height: 150px;
		text-align: center;
	}
	
	.content-text {
		font-size: 14px;
		color: "#000000";
	}
	
	.color-tag {
		width: 25px;
		height: 25px;
	}
	
	.uni-list {
		flex: 1;
	}
	
	.uni-list-item {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex: 1;
		flex-direction: row;
		background-color: #FFFFFF;
	}
	
	
	.uni-list-item__container {
		padding: 12px 15px;
		width: 100%;
		flex: 1;
		position: relative;
		/* #ifndef APP-NVUE */
		display: flex;
		box-sizing: border-box;
		/* #endif */
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		border-bottom-style: solid;
		border-bottom-width: 1px;
		border-bottom-color: #eee;
	}
	
	.uni-list-item__content-title {
		font-size: 14px;
	}
>>>>>>> 581906dc5a75fb04c786292dec069b0404f87f7e
</style>
