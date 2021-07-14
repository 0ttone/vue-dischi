<template>
  <div id="app">
        <Header/>
        <Main :library="libray"/>
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
        Main
    
  },
data() {
            return {
      library:[]
                  
            }
      },

created (){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
              this.library= result.data.response
        })
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
