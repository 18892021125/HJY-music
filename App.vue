<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	
	@import "/wxcomponents/vant/common/index.wxss";
	@import "/wxcomponents/vant/tabbar-item/index.wxss";
	@import "/wxcomponents/vant/tabbar/index.wxss";
	@import "/wxcomponents/vant/tab/index.wxss";
	@import "/wxcomponents/vant/tabs/index.wxss";
	@import "/static/iconfont.css";
</style>
