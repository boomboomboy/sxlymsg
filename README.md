# Cplugin 插件库
本插件目前仅支持vue

### npm 下载
		npm i vue-cplugin


### 提示消息message  可传显示文本参数

 		message共有3个方法 为全局注册的插件，可通过this.$message调用 或Vue.$message
 		this.message.success()
 		this.message.warning()
 		this.message.error()

        
### 加载  可传显示文本参数
		this.$Cloading(text)
### c-table 表格 
		props:{
		 tableData:[],//表格数据
		 thList:[] //表头，按序加载
		}
### c-form 表单
		props:[] //空  前面未做配置
### c-form-item 表单项
		props:{
		  label:'',
		}
		label通过slot实现  name为'label' 可通过插槽自定义
### c-input 输入框
		props:{
		  type:'',
		  readonly:Boolean，
		  prefix_icon:'', //input内容前的图标
		  suffix_icon:'',//input内容后的图标
		}
		input的值可通过v-model绑定 type接受原生input类型 暂未二次封装
### c-select 选择器
		props:{
		  selectData:[{value:'',name:''}],
		}
		select接受一个数组，内部引入c-drop-down组件件，该组件尚未开放，目前容器最多显示5组数据，超出则滚动显示，后续待优化
