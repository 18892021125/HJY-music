<template>
	<view class="index">
			
			<scroll-view class="scroll-view_H" scroll-x="true" @scroll="scroll" scroll-left="0">
				<view class="scrollitem" v-for="(val,index) in gundong.list" :key="index" @tap="goUrl('./pages/user/user')">
					<image class="scrollimg" src ="../../static/img/2.jpeg" ></image>
					<view v-if="val.titleone" class="info">
						<text >{{val.titleone}}<br>{{val.titletow}}</text>
					</view>
				</view>
			</scroll-view>
		

	</view>
</template>

<script>
	export default {
		data() {
			return {
			scrollTop: 0,
			old: {
				scrollTop: 0
			},
			gundong:{
					title:"滚动信息",
					list:[
						{titleone:"丝竹鼓乐",titletow:"沪上盛典",src:"../../static/img/2.jpeg"},
						{titleone:"民族音乐",titletow:"真滴牛批",src:"../../static/img/2.jpeg"},
						{titleone:"丝竹鼓乐",titletow:"真滴·牛B",src:"../../static/img/2.jpeg"},
						{titleone:"民族·音乐",titletow:"牛~~~~B",src:"../../static/img/2.jpeg"},
						
						
					]
				}
		}
	},
		methods: {
			scroll: function(e) {
				console.log(e)
				this.old.scrollTop = e.detail.scrollTop
			},
		}
}

</script>

<style lang="scss">
	.scrollimg{
		
		position: relative;
		width: 500rpx;
		height: 300rpx;
		border-radius: 35rpx;
		margin-left: 35rpx;
		
		padding-bottom: 0;
	}
	
		
		
	.scroll-view_H{
		
		background-color: #000000;
	}
	.scrollitem{
	background-color: #ffe8e6;
	display: inline-block;
	
	
	}
	.info{
		position: relative;
		left: 100rpx;
		
		bottom:250rpx;
		font-weight: bold;
		color: #FFFFFF;
		font-size: 40rpx;
	
		width: 200rpx;
		
	}
	
	
		
	
	.scroll-view_H {
		white-space: nowrap;
		height: 350rpx;
	}
	
	
	
</style>

