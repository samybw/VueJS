<template>
    <div class="header">
  <h1>{{titre}}</h1>
  <p>Sombre et sale </p>
</div> 
</template>
<script>

export default {
    name : 'Header',
    data() {
        return {
            titre : "le site de l'empereur"
        }
    },

 
}
</script>
<style scoped>
.header {
  padding: 30px;
  text-align: center;
  background: #1abc9c;
  color: white;
  font-size: 30px;
}
</style>>
    
