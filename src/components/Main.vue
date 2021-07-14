<template>
      <div Main class="container">
            <Album v-for="(album, index) in library"
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

</style>
