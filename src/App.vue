<template>
  <div id="app">
    <div class="container">
      <div class="row">Ciaone</div>
    </div>
    
    <Header/>
    <Albums/>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Albums from "./components/Albums.vue"

export default{
  name:"App",
  components:{
  Header,
  Albums
  }
}
</script>

<style lang="scss">
@import "./assets/style/common"
</style>
