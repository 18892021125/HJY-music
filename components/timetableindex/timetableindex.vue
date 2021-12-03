<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="我的课程" backgroundColor="#f8eee2" ></uni-nav-bar>
		<timetable :timetables="timetables"></timetable>
	</view>
</template>

<script>
	import timetable from '../../components/timetable/timetable';
	import {uniNavBar} from '@dcloudio/uni-ui';
	export default {
		components:{
			timetable,
			uniNavBar,
		},
		data() {
			return {
				timetables: [
				                  ['何家营鼓乐', '', '排练', '', '', '', '排练', '排练', '', '', '', '排练'],
				                  ['', '', '何家营鼓乐', '何家营鼓乐', '何家营鼓乐', '何家营鼓乐', '', '', '', '', '', ''],
				                  ['何家营鼓乐', '何家营鼓乐', '何家营鼓乐', '何家营鼓乐', '', '', '', '', '', '', '', ''],
				                  ['', '', '', '', '', '', '', '', '', '', '', ''],
				                  ['', '', '', '', '', '', '', '', '', '', '', '']
				                ]
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
