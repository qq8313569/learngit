2018.11.08  vue 于构建用户界面的渐进式框架
1.引用 script标签中引入vue.js文件
2. 核心基础语法
html 中
<div id="app">
  {{ message }}
</div>
js中
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }，
  methods：{自定义方法集}
})

3.基础命令
条件 v-if   循环 v-for  点击 v-on:click   缩写@click
一次性插值（也就是说值只会渲染1次后续更改变量的值不会同步在渲染上）v-once
渲染html数据 v-html
渲染元素属性 <div v-bind:id="dynamicId"></div>

4.vue的生命周期
beforeCreate：创建vue实例前
created:创建vue实例后  可以在此处获取其它非固定的数据 比如从服务器读取数据，或者申明其它变量
beforeMount:挂载到dom前
mounted：挂载到dom后
beforeUpdate：数据变化更新前
updated：数据变化更新后
beforeDestroy：vue实例3销毁前
destroyed：实例销毁后

二 vue与后台数据交互插件axios
基础语法 axios.post(链接php地址文件，｛传递参数｝).then(function(res){返回数据为一个对象其中data是传递的数据内容 其它的是数据传输的header设置信息})
后台传输方式为文件流传输 需用json_decode转换 json_decode(file_get_contents('php://input'),1);

心得：vue好用？  不存在的  没熟悉之前好用何从谈起