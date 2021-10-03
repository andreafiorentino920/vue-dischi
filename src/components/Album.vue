<template>
  <div class="album text-center mb-5 p-3">
    <div class="poster">
      <img :src="info.poster">
    </div>
    
    <span class="title pt-2">{{info.title}}</span><br>
    <span class="author">{{info.author}}</span><br>
    <span class="year">{{info.year}}</span>
  </div>
</template>

<script>
    export default{
      props: {
          info: Object
        },
      name:"Album"
    }
</script>

<style lang="scss" scoped>
.album{
  background-color: #2e3a46;
  height: 300px;
  .poster{
    img{
      max-width: 100%;
    }     
  }
  
.title{
  color: white;
  text-transform: uppercase;
  display: inline-block;
}
.author, .year{
  color: #808080;
  font-size: 13px;
}
}

</style>>
