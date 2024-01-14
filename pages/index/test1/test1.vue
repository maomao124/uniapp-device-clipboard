<template>
	<view>
		<input style="background-color: antiquewhite;" placeholder="内容" type="text" v-model="value"/>
		<button type="primary" @click="set">复制</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				value:''
			}
		},
		methods: {
			set()
			{
				uni.setClipboardData({
					data:this.value,
					success: () => {
						console.log('成功');
					},
					fail: () => {
						console.log('失败');
					}
				})
			}
		}
	}
</script>

<style>

</style>
