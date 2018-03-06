```javascript
<template>
<input v-model='value' />
{{myvalue()}} 
</template>


new Vue(
	data:() {
		value: ''
	},
	computed: {
		myvalue(){
			return this.value.repalce(/\d/g, '')
			//若想动态变化 必须与data对应
		}	
	},
	watch: {
		value: function(val, oldVal){
			console.log(val, oldVal)
		}
	}
)
```

#自定义事件v-on 事件绑定
简写@, 自定义事件@my-event。子父组件传递消息方法
v-on修饰符可以指定键盘事件
1. emit


# v-model  与单、复选，下拉列表的双向绑定
表单数据双向绑定

v-model支持的三种修改器
1. v-model.lazy  失焦 之后更新 而不是立即更新
2. v-model.number  不使用的时候对应绑定的数据是字符串
3. v-model.trim  裁剪前后多余的空格

## 计算属性 computed
更data设定的属性一样
