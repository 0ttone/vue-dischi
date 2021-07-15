<template>
      <div  class="container ">
            <Album class="col-personal album-item"
            v-for="(album, index) in library"
            :key="index"
            :album="album"/>





      </div>
</template>

<script>

import Album from './Album.vue'


export default {
      name: 'Main',
      components: {
            Album
      },
      props: {
            library: Array,
      }
}

</script>


<style lang="scss" scoped>
@import "./style/_color.scss";


</style>
