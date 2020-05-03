<template>
	<view>
		<text>这是一个text组件</text>
		<text>
			{{msg}}
		</text>
		<button type="primary" @tap="test">event</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		props:["msg"],
		methods: {
			test(){
				// this.$emit("showName",{name: "chujian"})
				uni.$emit("showAge",{age: 20})
			}
		}
	}
</script>

<style lang="scss">

</style>
