<script>
	import config from '@/app.config.js'
	export default {
		methods: {

		},
		// 监听 - 页面404
		onPageNotFound:function(e) {
			uni.redirectTo({
				url: config.error.url
			})
		},
		onLaunch: function() {
			if(config.debug) console.log('App Launch')
			let that = this;
		},
		onShow: function() {
			if(config.debug) console.log('App Show')
		},
		onHide: function() {
			if(config.debug) console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import "./uni_modules/vk-uview-ui/index.scss";
	/* 自定义全局css */
	@import "./common/css/app.scss";
</style>
