<template>
	<view class="index">
	<br>
	
	<br>
	
	<uni-search-bar placeholder="乐谱搜索" :radius="100"  @confirm="search"></uni-search-bar>
	<font class="guesslike">猜你喜欢</font>
	<jingxuangundong></jingxuangundong>
	
<van-tabs v-model:active="active">
  <van-tab title="标签 11">666</van-tab>
  <van-tab title="标签 2">内容 2</van-tab>
  <van-tab title="标签 3">内容 3</van-tab>
  <van-tab title="标签 4">内容 4</van-tab>
</van-tabs>
	
	</view>
</template>

<script>
	import jingxuangundong from '@/components/jingxuangundong/jingxuangundong';
	import {ref} from '../../vue.js';
	import jiaoliu from '@/components/jingxuan/jiaoliu';
	import yuanchuang from '@/components/jingxuan/yuanchuang';
	import yanchu from '@/components/jingxuan/yanchu';
	import tuijian from '@/components/jingxuan/tuijian';
	export default {
		data() {
			return {
			
			}
		},
		setup() {
		    const active = ref(0);
		    return { active };
		  },
		methods: {
			
		
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #aaaaff;
	}
		
	ul{
		list-style-type: none;
		text-align: center;
		margin:0;
		
	}
	li{
		display: inline-block;
		margin:0 10rpx;
	}
	
</style>
