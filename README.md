# wxcomponents

微信小程序自定义五级联动组件

使用方式

自定义组件地址组件，使用第三方地址包，可以任意更改样式，生成符合自己喜好的样式，更加符合项目的需要

使用方式如下

首先需要在wxml中引入 （其中的事件绑定名称可以在组件js中进行修改）

/**<area-select id="areaSelect" bind:cancelEvent="_cancelEvent" bind:confirmEvent="_confirmEvent"> </area-select>**/
其次需要在引入组件的js中定义该组件(onReady)

this.areaSelect=this.selectComponent("#areaSelect");

最后一点一定要在json文件中添加插件的地址

"usingComponents":{"area-select": "/components/area-select/area-select"}

做完这些后就是在js中绑定好事件

取消事件：_canceEvent

确认事件：_cnnfirmEvent

地址组件的最重要的参数即是 this.areaSelect.data.addressObj

比较重要的一点就是显示地址选择框

this.areaSelect.showDialog();

this.areaSelect.hideDialog();

创作于20180308-by-张涛
