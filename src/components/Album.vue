<template>
      
      
      <div>{{album.title}}</div>
      <div>{{album.author}}</div>
      <div>{{album.genre}}</div>
      <div>{{album.year}}</div>
      
      
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
