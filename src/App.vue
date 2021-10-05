<template>
  <div id="app">
    <header>
      <Header @selectGenres="selectGenres"/>
    </header>
    <main>
        <div class="container">
          <Albums :selectedGenre="selectedGenre"/>
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
  },
  data(){
    return{
      selectedGenre: ""
    }
  },
  methods:{
    selectGenres(selectedGenre){
    this.selectedGenre = selectedGenre
    }
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
