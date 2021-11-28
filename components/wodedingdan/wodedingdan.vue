<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="我的订单" backgroundColor="#f8eee2" ></uni-nav-bar>
		<view class="uni-padding-wrap uni-common-mt">
			<uni-segmented-control :current="current" :values="items" :style-type="styleType"
				:active-color="activeColor" @clickItem="onClickItem" />
		</view>
		<view class="content">
			<view v-if="current === 0"><daifukuan></daifukuan></view>
			<view v-if="current === 1"><daifahuo></daifahuo></view>
			<view v-if="current === 2">333</view>
		</view>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import {uniSegmentedControl} from '@dcloudio/uni-ui';
	import daifukuan from '../../components/daifukuan/daifukuan';
	import daifahuo from '../../components/daifahuo/daifahuo';
	
	export default {
		components:{
			uniNavBar,
			uniSegmentedControl,
			daifukuan,
			daifahuo,
		},
		data() {
			return {
				items: ['待付款','待发货','待收货','退货'],
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
			onClickItem(e) {
				if (this.current !== e.currentIndex) {
					this.current = e.currentIndex
				}
			},
		}
	}
</script>

<style lang="scss">
	page{
		background-color: #f8eee2;
	}
.content{
	background-color: #FFFFFF;
	height: 100%;
	width: 100%;
	position: absolute;
	margin-top: 30rpx;
	border-top-left-radius: 55rpx;
	border-top-right-radius: 55rpx;
	
}
</style>
