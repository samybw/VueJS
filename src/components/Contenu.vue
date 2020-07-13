<template>
  <div class="container">
   <h1>Appel d'une API</h1>

    <img v-bind:src="urlImg">


  </div>
  
</template>
<script> 

import axios from 'axios'

      export default {
          name: 'continue',
          data: function () {
              return {
                 urlImg : null,

              }
                
           },
           methods: {
           
           },
           mounted() {
             axios
             .get('https://api.thecatapi.com/v1/images/search')
             .then(response => {
               console.log(response);
               this.urlImg = response.data[0].url
             }) 
           },
        }



</script>


