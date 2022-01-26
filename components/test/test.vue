<template>
	<view class="test" :style="{color:color}" @click="onClick">
		<slot></slot>
	</view>
</template>

<script>
	export default {
		name:"test",
		props:{
			color:{
				type:String,
				default:'#000'
			}
		},
		data() {
			return {
				
			};
		},
		methods:{
			onClick(){
				console.log('test组件点击');
				this.$emit('change', this.color)
			}
		},
		// 组件生命周期
	}
</script>

<style>
	.test{
		width: 200rpx;
		height: 100rpx;
		text-align: center;
		line-height: 100rpx;
		border: 1rpx red solid;
	}
</style>
