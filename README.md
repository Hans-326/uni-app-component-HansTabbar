# uni-app-component-HansTabbar
##使用方法
###在script中引入组件
```
import hansTabber from '../../components/hans-tabbar/hans-tabbar.vue'
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
		methods: {
			tabChange(index) {
				console.log(index)
			}
		}
```
###在 template 中使用组件
```
<hans-tabber :list="list" style="position:fixed;bottom:0;width:100%;left:0;right:0;" @tabChange="tabChange"></hans-tabber>
```

##属性说明
| 属性名        | 类型    |  必填  | 说明|
| --------   | -----:   | :----: |--------|
| list        | Array     |   是    |text为tabbar显示名称；iconPath:默认显示icon地址；selectedIconPath:选中状态icon地址 |

##事件说明
| 事件名称        | 说明    |  返回  | 
| --------   | -----:   | :----: |
| tabChange        | 点击tabbar的事件     |   当前点击的index    |
