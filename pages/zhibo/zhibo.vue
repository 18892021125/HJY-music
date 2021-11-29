<template>
	<view>
		<uni-nav-bar
			left-icon="back"
			@clickLeft="back"
			backgroundColor="#00000000"
			style="position: absolute; z-index: 999999;">
		
		</uni-nav-bar>
		<dt-video :list="videos"></dt-video>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import dtVideo from "@/components/dt-video/dt-video"
	
	export default {
		components:{
			uniNavBar,
			dtVideo
		},
		data() {
			return {
				list: [{
							iconPath: "home",
							selectedIconPath: "home-fill",
							text: '首页',
							count: 2,
							isDot: true,
							customIcon: false,
						}],
		
				videos: [
					{
						title:'何家营直播',
						desc:"乐手们正在表演中！",
						src: "http://img.zhangjunbo.top/202111291728%281%29.mp4"
					},
					{
						title:'何家营直播',
						desc:"乐手们正在表演中！",
						src: "http://img.zhangjunbo.top/202111291728%281%29.mp4"
					},{
						title:'何家营直播',
						desc:"乐手们正在表演中！",
						src: "http://img.zhangjunbo.top/202111291728%281%29.mp4"
					},
					
				],
			
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

</style>
