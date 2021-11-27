<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="设置" backgroundColor="#f8eee2" ></uni-nav-bar>
		<br>
		<br>
		<view class="liebiaoindex">
			<uni-list>
				<br>
				<uni-list-item title="账号管理" :border="false" />
				<br>
				<uni-list-item title="修改绑定手机" :border="false" rightText=">" />
				<br>
				<uni-list-item title="设置密码" :border="false" rightText=">" />
				<br>
				<uni-list-item title="微信绑定"   rightText="未绑定>"/>
				<br>
				<uni-list-item title="支付宝绑定" :border="false" rightText="未绑定>" />
				<br>
				<uni-list-item title="网络设定"  />
				<br>
				<uni-list-item title="自动流量播放"  :show-switch="true" :border="false" />
				<br>
				<uni-list-item title="注销账号" :border="false" rightText=">" />
				<br>
			</uni-list>
			
		
		</view>
	</view>
</template>

<script>
	import {uniList} from '@dcloudio/uni-ui';
	import {uniListItem} from '@dcloudio/uni-ui';
	import {uniNavBar} from '@dcloudio/uni-ui';
	export default {
		components:{
			uniList,
			uniListItem,
			uniNavBar,
		},
		data() {
			return {
				
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

<style>
	page{
		background-color: #FFFFFF;
		
	}
.liebiaoindex{
	border-top-left-radius: 35rpx;
	border-top-right-radius: 35rpx;
	margin: 30rpx;
	
}

</style>
