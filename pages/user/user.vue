<template>
	<view class="index">
		
		<student></student>
	</view>
	
</template>

<script>
	import teacher from '@/components/teacher/teacher';
	import student from '@/components/student/student';
	export default {
		components:{
			student,
		},
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
	background-color: #F8EEE2;
	height: 999rpx;
}
</style>
