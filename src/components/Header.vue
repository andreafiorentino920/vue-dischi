<template> 
  <div class="header-bar d-flex flex-row align-items-center">
    <div class="pt-3 pb-3 ps-2 me-auto">
      <img src="img/spotify-logo.png" alt="">
    </div>
    <form class="form d-flex">
            <select v-model="selectGenre" @change="$emit('selectGenres', selectGenre)">
                <option value="">Seleziona un genere</option>
                <option value="rock">Rock</option>
                <option value="pop">Pop</option>
                <option value="jazz">Jazz</option>
                <option value="metal">Metal</option>
            </select>
    </form>
  </div>
</template>

<script>
    export default{
        name:"Header",
        props:["img"],
        data(){
          return {
            selectGenre:""
          }
        }
      }
</script>

<style lang="scss" scoped>
  .header-bar{
    background-color: #2E3A46;

    img{
      width: 8%;
    }
  }
</style>

