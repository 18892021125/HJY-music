<template>
	<view >
		<view class="music" v-for="(val,index) in prodata.list" :key="index" @tap="goUrl('../info/index')">
			<view class="musicitem">
				<image v-if="val.src" :src="val.src" style="width: 80px; height: 80px; ">
				<view class="textinfo">
					<br>
					<font v-if="val.typec" class="typec">{{val.typec}}</font>
				    
					<font v-if="val.typee" class="typee">{{val.typee}}</font>
					
				</view>
				<view class="playicon" >
					<uni-icons custom-prefix="iconfont" type="icon-bofang" size="50" @click="playmusic" ></uni-icons>
				</view>		
			</view>
		</view>
	</view>
	
</template>

<script>
	export default {
		props:{
			prodata: {
				type: String,
				default: []
			},
		},
		data() {
			return {
			
		}
	},
		methods:{
			playmusic(){
				
			}
		}
	}
</script>

<style>
		
	
.textinfo{
	margin-left: 20px;
	display: flex;
	flex-direction: column;
}
.playicon{
	display: inline;
	
	margin-bottom: 15px;
	margin-left: 70px;
	float: right;
	padding-top: 20px;

}
.type{
	color: #FF6034;
	face:"黑体";
}
.typec{
	color: #000000;
	font-weight: bold;
}
.typee{
	color: #969799;
	font-size: small;
}

.musicitem{
	display: flex;
	flex-direction: row;
	
}
.music{
	margin-top:8px ;
	background-color: #fffcf3;
	border-radius: 25px;
	flex-direction: row;
}
</style>
