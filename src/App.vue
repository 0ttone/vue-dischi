<template>
  <div id="app">
        <Header/>
        <Main :library="library"/>
  </div>
</template>

<script>

import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';


export default {
  name: 'App',
  components: {
        Header,
        Main,
    
  },
data: function() {
            return {
      library:[]
                  
            }
      },

created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
              this.library= result.data.response
        })
  }
}
</script>

<style lang="scss">
@import "./style/app.scss";
#app{
      background-color: $bg-primary-color;
}


</style>
