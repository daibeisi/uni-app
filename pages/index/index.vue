<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<test color="red" @change="change">测试组件</test>
		
		<!-- #ifdef H5 || APP-PLUS -->
		<view class="text-area">
			<text class="title">我只在H5或者APP中展示</text>
		</view>
		<!-- #endif -->
		
		<!-- #ifdef MP-WEIXIN -->
		<view class="text-area">
			<text class="title">我只在微信小程序中展示</text>
		</view>
		<!-- #endif -->
	</view>
</template>

<script>
	import test from "@/components/test/test.vue"
	export default {
		components:{
			test
		},
		data() {
			return {
				title: '首页'
			}
		},
		// 页面生命周期
		onInit() {
			console.log('监听页面初始化，其参数同 onLoad 参数，为上个页面传递的数据，参数类型为 Object（用于页面传参），触发时机早于 onLoad')
		},
		onLoad() {
			uni.getSystemInfo({
				success(res) {
					console.log('获取系统信息成功', res);
				},
				fail(err) {
					console.log('获取系统信息失败', err)
				},
				complete() {
					console.log('获取系统信息完成')
				}
			})
		},
		onShow() {
			console.log('监听页面显示。页面每次出现在屏幕上都触发，包括从下级页面点返回露出当前页面')
		},
		onReady() {
			console.log('监听页面初次渲染完成。注意如果渲染速度快，会在页面进入动画完成前触发')
		},
		onHide() {
			console.log('监听页面隐藏')
		},
		onUnload() {
			console.log('监听页面卸载')
		},
		onResize() {
			console.log('监听窗口尺寸变化')
		},
		onPullDownRefresh() {
			console.log('监听用户下拉动作，一般用于下拉刷新')
		},
		onReachBottom() {
			console.log('页面滚动到底部的事件（不是scroll-view滚到底），常用于下拉下一页数据')
		},
		methods: {
			onClick(){
				console.log('11111111')
			},
			change(e){
				console.log('我是页面的事件，我返回了：' + e)
			}
		}
	}
</script>

<style>
	@import './index.css';
	/* page等价于body,开发布局建议使用flex,尺寸单位可用:px rpx rem vh vw* */
	page {
		background-color: #F8F8F8;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
