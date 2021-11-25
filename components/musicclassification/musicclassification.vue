<template>
	<view >
		<view class="music" v-for="(val,index) in prodata.list" :key="index" @tap="goUrl('./pages/user/user')">
			<view class="musicitem">
				<image v-if="val.src" :src="val.src" style="width: 70px; height: 70px;margin-top: 15rpx;margin-left: 15rpx;margin-bottom: 15rpx; ">
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
	
		data() {
			return {
			prodata:{
				title:"音乐信息",
				list:[
					{typec:"木管乐器1",typee:"Woodwind instrument1",src:"../../static/img/muguan.png"},
					{typec:"木管乐器2",typee:"Woodwind instrument2",src:"../../static/img/muguan.png"},
					{typec:"木管乐器3",typee:"Woodwind instrument3",src:"../../static/img/muguan.png"},
					{typec:"木管乐器4",typee:"Woodwind instrument4",src:"../../static/img/muguan.png"},
					{typec:"木管乐器5",typee:"Woodwind instrument5",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"},
					{typec:"木管乐器6",typee:"Woodwind instrument6",src:"../../static/img/muguan.png"}
				]
			}
		}
	},
		methods:{
			playmusic(){
				
			}
		}
	}
</script>

<style lang="scss">
		
	
.textinfo{
	margin-left: 20px;
	display: flex;
	flex-direction: column;
}
.playicon{
	display: inline;
	
	margin-top: auto;
	margin-bottom: auto;
	margin-left: auto;
	margin-right: 19rpx;
	float: right;
	

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
	margin-top:15rpx ;
	background-color: #fffcf3;
	border-radius: 25px;
	flex-direction: row;
	margin-left: 25rpx;
	margin-right: 25rpx;
}
</style>
