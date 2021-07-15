<template>
      <div>
            <img
                  :src="album.poster"
                  :alt="`Album title: ${album.title}, Author: ${album.author}`" > 
                  <div><h5>{{album.title}}</h5></div>
                  <div><h6>{{album.author}}</h6></div>
                  <div><h6>{{album.year}}</h6></div>
                  <div><h6>{{album.genre}}</h6></div>

      </div>   
</template>
      
 
<script>
export default {
      name: 'Album',
      props:{
            album: Object,
      }
}

</script>


<style lang="scss" scoped>

</style>
