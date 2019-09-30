<template>
  <div class="container">
    <app-header></app-header>
    <hr>
    <div class="row">
      <app-servers></app-servers>
      <app-server-detail></app-server-detail>
    </div>
    <hr>
    <app-footer></app-footer>
  </div>
</template>

<script>
  import Header from "./components/Shared/Header";
  import Footer from "./components/Shared/Footer";
  import Servers from "./components/Server/Servers";
  import ServerDetail from "./components/Server/ServerDetail";
  export default {
    components:{
      'app-header': Header,
      'app-servers': Servers,
      'app-server-detail': ServerDetail,
      'app-footer': Footer
    }
  }
</script>

<style>

</style>
