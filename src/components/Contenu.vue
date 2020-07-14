<template>
  <div class="container">
   <h1>Formulaire</h1>

   <form >
   
   <label for="prenom"> Prenom </label>
  <input v-on:input="toggleResult" v-model="formData.prenom" type="prenom" name="prenom" id="prenom">
  <br>
  <br>
  <label for="txt"> Textarea</label>
  <textarea v-model="formData.txt" id="txt" ></textarea>
   



            <h3>Checkbox</h3>
               <div>
     <label for="fraise"> Fraise</label>
     <input v-model="formData.checkFruits" value="fraise" type="checkbox"  id="fraise">

   </div>

    <div>
     <label for="pomme"> Pomme </label>
     <input v-model="formData.checkFruits" value="pomme" type="checkbox"  id="pomme">

   </div>
   
    <div>
     <label for="cerises"> Cerises</label>
     <input v-model="formData.checkFruits" value="cerises" type="checkbox"  id="cerises">


        
        <h3>Select Box </h3>
        <select v-model="formData.select">
          <option v-for="(pays, index) in formData.listePays " :key="index" > {{ pays }}</option>
        </select>

         
   </div>
    <br>
    <button v-on:click.prevent="envoiForm" type="submit"> Envoyer les données</button>
   <br>
   </form>
   
   <br>

   <div v-if="infoSubmit">
      <h2>Resultat</h2>

   <p>Prenom : {{ formData.prenom }}</p>
   <p>Text : {{ formData.txt }}</p>
          <ul>
         <li v-for="(fruits, index) in formData.checkFruits" :key="index"> {{ fruits }} </li>
       </ul>
   <p>Pays : {{ formData.select}}</p>

   </div>



  </div>
  
</template>
<script> 


      export default {
          name: 'continue',
          data: function () {
              return {
                formData: {
                 prenom : '',
                 txt: '',
                 checkFruits : [],
                 select: '',
                 listePays : ['CongoRDC' ,'Chine','Sénégal','USA']
                },
                infoSubmit: false

              }
                
           },
           methods: {
             envoiForm: function (){
                this.infoSubmit = true;
             },

             toggleResult: function () {
               this.infoSubmit = false
             }
           
           },
    
        }



</script>


