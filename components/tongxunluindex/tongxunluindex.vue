<template>
	<view>
		<uni-nav-bar left-icon="back" @clickLeft="back" title="通讯录" backgroundColor="#f8eee2" ></uni-nav-bar>
		
		<tongxunlu @ev="evFunc" :datas="datas" color="red" :index="true" name="employeeName"></tongxunlu>
	</view>
</template>

<script>
	import {uniNavBar} from '@dcloudio/uni-ui';
	import tongxunlu from '@/components/tongxunlu/tongxunlu';
	export default {
		components:{
			tongxunlu,
			uniNavBar,
		},
		data() {
			 let datas = [{
			        "employeeId": "test1",
					"employeeName": "Charlie Puth",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Rihanna",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Adele",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Shawn Mendes",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Bruno Mars",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Ed Sheeran",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    },{
			        "employeeId": "test1",
					"employeeName": "Troye Sivan",
					"companyId": "1",
					"companyName": "test company",
					"departmentId": "testdeptid",
					"departmentName": "西北大学",
					"postId": "testpostid",
					"postName": "testpost",
			    }
				]
			        return {
			            datas:datas
			        };
		},
		methods: {
		        evFunc(data){
		            console.log(data)
		        },
				back() {
					uni.navigateBack({
						delta: 1
					})
				},
		    },
		 mounted() {
		    }
	}
</script>

<style lang="scss">

</style>
