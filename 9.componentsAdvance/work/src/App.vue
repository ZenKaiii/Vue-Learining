<template>
  <div class="container">
    <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent='appNew'">New</button>
        <hr>
        {{selectedComponent}}
        <keep-alive>
            <component :is="selectedComponent"></component>
        </keep-alive>
<!--      <app-quote>-->
<!--          <h2 slot="title">Quote</h2>-->
<!--          <p slot="content">A wonderful quote</p>-->
<!--      </app-quote>-->
    </div>
  </div>
</template>

<script>
  import Quote from "./components/Quote";
  import Author from "./components/Author";
  import New from "./components/New";
  export default {
      data(){
          return {
              selectedComponent: 'appQuote'
          }
      },
    components:{
      appQuote : Quote,
      appAuthor: Author,
      appNew: New
    }
  }
</script>

<style>


</style>