<script>
	export default {
		// 应用生命周期
		onLaunch: function() {
			console.log('App Launch','当uni-app 初始化完成时触发（全局只触发一次）')
		},
		onShow: function() {
			console.log('App Show','当 uni-app 启动，或从后台进入前台显示')
		},
		onHide: function() {
			console.log('App Hide','当 uni-app 从前台进入后台')
		},
		onError:function(){
			console.log('App Error','当 uni-app 报错时触发')
		},
		onUniNViewMessage:function(){
			console.log('对 nvue 页面发送的数据进行监听')
		},
		onUnhandledRejection:function(){
			console.log('对未处理的 Promise 拒绝事件监听')
		},
		onPageNotFound:function(){
			console.log('页面不存在监听函数')
		},
		onThemeChange:function(){
			console.log('监听系统主题变化')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
