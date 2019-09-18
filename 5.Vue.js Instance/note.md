# Vue.js Instance

- vue instance 是DOM(HTML)与业务逻辑的中间件
- 我们将业务逻辑封装到vue实例中

#### 1. 使用多个vue实例

- 在同一页面中，可以使用多个vue实例控制不同的部分
- 实例之间没有联系 

#### 2. 从外部访问vue实例

- 从一个实例内访问另一个实例是可行的
- 也可以从js代码中访问vue实例

#### 3. Vue代理

- vue代理了我们在data里设置1的属性(包括methods computed)，因此我们可以在外部访问到

#### 4. $el, $data, $refs

- $el: 指代Vue实例控制的HTML模板
- $data：可以使用外部对象初始化
- $refs: 注册的组件，可以通过this.$refs.myButton. xxx 访问 前提 ref=“myButton”

#### 5. 挂载模板

- vm.$mount("#app") 与el 功能一样

#### 6. Vue如何在监测变化后更新页面

- Vue实例与DOM之间有一层虚拟DOM
- 通过更改虚拟DOM，并与DOM对比，改变对应部分

#### 7. Vue实例生命周期

1. new Vue() 
2. beforeCreate(): 初始化数据
3. created()
4. 编译模板
5. beforeMount()
6. 模板挂载到DOM上 -> 数据更新 -> 重新渲染 -> 重新挂载
7. destroyed()