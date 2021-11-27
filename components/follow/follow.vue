<template>
	<view class="index">
	
		<uni-search-bar placeholder="搜索" :radius="100" :class="searchbar" @confirm="search" ></uni-search-bar>
		
		<usercard :prodata="follows"></usercard>
	
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	
	.index{
		background-color:#F8EEE2;
		padding-top: 60rpx;
	}
</style>
