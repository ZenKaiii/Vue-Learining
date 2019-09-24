# vue cli 

### 1. vue命令行

- 可以帮助我们获取vue项目模板

- ``` npm install -g @vue/cli```

- ```shell
  vue create demo
  npm run serve 有别于vue-cli2
  ```

### 2. 单文件组件

```javascript
import Vue from 'vue'
import App from './App.vue'

Vue.config.productionTip = false

new Vue({
  render: function (h) { return h(App) },
}).$mount('#app')
```

- 获取指定dom，渲染App组件

  ```html
  <template>
  
  </template>
  
  <script>
  export default {
  }
  </script>
  
  <style>
  
  </style>
  
  ```

  - 三部分



