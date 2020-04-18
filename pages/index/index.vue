<template>
	<hans-tabber :list="list" style="position:fixed;bottom:0;width:100%;left:0;right:0;" @tabChange="tabChange"></hans-tabber>
</template>

<script>
	import hansTabber from '../../components/hans-tabbar/hans-tabbar.vue'
	export default {
		components:{
			hansTabber
		},
		data() {
			return {
				list: [{
					 "text": "未录入",
					 "iconPath": '../../static/enter.png' ,
					 "selectedIconPath": '../../static/enter-select.png'
				   },
				   {
					 "text": "作业互评",
					 "iconPath": '../../static/correct.png',
					 "selectedIconPath":'../../static/correct-select.png'
					 },
					 {
					   "text": "成绩分析",
					   "iconPath": '../../static/analyse.png',
					   "selectedIconPath": '../../static/analyse-select.png'
					 }],
			}
		},
		onLoad() {

		},
		methods: {
			tabChange(index) {
				console.log(index)
			}
		}
	}
</script>

<style>
</style>
