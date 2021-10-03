<template>
  <div id="app">
    <Header/>
    <main>
        <div class="container">
          <Albums/>
        </div>
        
    </main>
    
    

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
@import "./assets/style/common";
#app{
  main{
  background-color: #1E2D3B;
  padding-top: 100px;

  .container{
    width: 80%;
  }
}
}

</style>
