# 组件

## 1. 组件介绍

- 可重用模板，可复用的vue实例

- 组件继承了vue实例

- ```vue
  Vue.component("标签名",{
  	data(){
  		return {
  			status:"ccc"
  		} ##这里data是函数，返回新对象
  	},
  	template: `<p>{{status}}</p>`
  })
  ```

- Vue.component()注册全局组件

- 局部组件如下

- ```js
  var cmp = {
     data(){
  		return {
  			status:"ccc"
  		} //这里data是函数，返回新对象
  	},
  	template: `<p>{{status}}</p>` 
  }
  new Vue({
      el:"#app",
      components:{
          "my-cmp": cmp
      }
  })
  ```

- **App.vue** 是根组件

- 自定义组件，模板只能有一个根元素 div