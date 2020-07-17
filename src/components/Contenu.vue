<template>
  <div class="container">
   <h1>Quoi de prevu ?</h1>
<form action="">

<label for="action"></label>
<input type="text" v-model="tache" id="action">


<button type="submit" v-on:click.prevent="creationItem"> Crée une Tache </button>

</form>



<ul>
  <li v-for="(tache, index) in tableauTaches" :key="index">
     <item :tache="tache" :suppression="suppression"> </item>
     </li>
</ul>
  

  
  



  </div>
  
</template>
<script> 

import Item from './Item'

      export default {
          name: 'Contenu',
          data: function () {
              return {
                formData: {
                    
                },
                tableauTaches : ["Js", "PHP", "Python","Angular"],
                tache: ""
              

              }
                
           },
           components:{
              'item': Item
           },
           methods: {
              creationItem : function() {
                this.tableauTaches.push(this.tache)
                this.tache = ""
              },
              suppression : function (e) {
                this.tableauTaches.splice(e.target.parentNode.id , 1)
              }
           
           },
    
        }



</script>

<style scoped>

ul {
  list-style-type: none;
  padding: 0;
}

</style>


