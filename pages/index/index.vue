<template>
	<view class="content">
		<view class="text-area">
			<test :msg="msg" @showName="testEvent"></test>
			<text class="title">{{title}}</text>
		</view>
		<view>
			{{"LILI"}}
		</view>
		{{name}}
		<view>
			{{"Milk.indexOf(lk)" !== -1 ? "chujian" : "galaxy"}}
		</view>
		<view 
			v-for="item,index in nameList" 
			:key="index"
			:style="[{width: '100px', height: '100px', background: 'pink'}]"
		>
			{{item}}
		</view>
	</view>
	
</template>

<script>
	import test from '../../components/text/text.vue'
	export default {
		
		data() {
			return {
				title: 'Hello',
				msg: "silver river",
				name: "lili",
				nameList: ['12','23','34','45']
			}
		},
		components: {
			test 
		},
		onLoad() {
			// uni.$on("showAge",(rel)=>{
			// 	console.log(rel)
			// })
			uni.$once("showAge",(rel)=>{
				console.log(rel)
			})
		},
		methods: {
			testEvent(name){
				console.log(name.name || name)
			}
		}
	}
</script>

<style lang="scss" scoped>
	
</style>
