<template>
  <section class="album-container container">
  <div class="row row-cols-5">
    <div class="col" :key="index" v-for="(album,index) in filterAlbums">
      <Album :info="album"/>
    </div>
  </div>
  </section>

</template>

<script>
    import axios from 'axios';
    import Album from "./Album.vue"
    export default{
        name:"Albums",
        components:{
            Album
        },
        props:["selectedGenre"],
        data(){
          return{
            albums:[],
          }
        },
        created(){
          axios
              .get("https://flynn.boolean.careers/exercises/api/array/music")
              .then((res) =>{
                this.albums = res.data.response;
              });
        },
        computed:{
          filterAlbums(){
            const arrFiltered = this.albums.filter(
              (elm) => {
                if(elm.genre.toLowerCase() == this.selectedGenre.toLowerCase() || this.selectedGenre == ""){
                  return true
                }
                return false
              }
            )
            return arrFiltered;
          }
        }
    }


</script>

<style lang="scss" scoped>

</style>