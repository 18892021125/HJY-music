<template>
	<view class="index">
	
		<uni-search-bar placeholder="搜索" :radius="100" :class="searchbar" @confirm="search" ></uni-search-bar>
		<scroll-view>
			<usercard :prodata="follows"></usercard>
		</scroll-view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				follows:{
					title:"关注列表",
					list:[
						{name:"user1",sign:"test sign",src:"../../static/img/follow1.png"},
						{name:"user2",sign:"test sign128888888",src:"../../static/img/follow2.png"},
						{name:"user3",sign:"test sign23",src:"../../static/img/follow1.png"},
						{name:"user4",sign:"test sign34",src:"../../static/img/follow2.png"},
						{name:"user5",sign:"test sign45",src:"../../static/img/follow1.png"},
						{name:"user6",sign:"test sign56",src:"../../static/img/follow2.png"},
						
						{name:"user7",sign:"test sign67",src:"../../static/img/follow1.png"},
						{name:"user8",sign:"test sign78",src:"../../static/img/follow2.png"},
						{name:"user9",sign:"test sign89",src:"../../static/img/follow1.png"},
						
					]
				},
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	
	.index{
		background-color:#f7ede2;
		padding-top: 60rpx;
	}
</style>
