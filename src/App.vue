<template>
  <div id="app">
    <header-top></header-top> 
    <contenu></contenu>
   
    
  </div>
</template> 
<script>

import Contenue from './components/Contenu.vue'
import Header from "./components/Header.vue"

export default {
  name: 'App',
  components: {
    'contenu': Contenue,
    'header-top': Header,
   

    
  
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>


