# 组件间通信

### 1. 父与子通信

#### 1. props

- 为了从父组件向子组件传递数据

- props表示由外层组件即父组件设置的属性

- props注册的属性，与普通属性一样使用，用this访问

- 验证props

  ```js
  props: {
       name: [String]
  }
  ```

- 通过在子组件中触发一个自定义事件，并在父组件中监听 （@事件名）-> 实现了把数据从子组件传递回父组件

- vue组件中的数据是单向流动的

  - 只能从父到子/子到父
  - 子之间无法直接通信

- 可以利用事件总线，实现子组件间通信

#### 2. 自定义事件

- 为了从子组件反向传递回父组件

#### 3. 回调函数

- 另一种子到父的通信
- 用props传递回调函数
- 回调函数实际上在父组件中执行，但用props让它可以在子组件内调用

### 2. 子与子通信

#### 1. 自定义事件，借由父组件完成

	#### 2. 利用回调

#### 3. 利用事件总线

- 原理：利用中央对象传递数据（服务）

- 在main.js中创建

  ```js
  export const eventBus = new Vue();
  
  
  import {eventBus} from '../main.js'
  
  eventBus.$emit('ageWasEdited',this.age)
  
  created()
  {
     	eventBus.$on('ageWasEdited', (age)=>{
     	this.age = age;
  	})
  }
  ```

- 