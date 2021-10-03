<template>
  <div class="logo-bar pt-3 pb-3 ps-2">
    <img src="img/spotify-logo.png" alt="">
  </div>
</template>

<script>
    export default{
        name:"Header",
        props:["img"]
    }
</script>

<style lang="scss" scoped>
  .logo-bar{
    background-color: #2E3A46;

    img{
      width: 3%;
    }
  }
</style>

