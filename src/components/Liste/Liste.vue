<template>
<div class="container md">


    <ul class="liste">
        <li v-for="(film, index) in myArr" v-bind:key="index"> 
            titre : {{ film.titre }} , date : {{ film.date }}

        </li>
    </ul>
<p>{{ txt }}</p>
  <div>
      <button v-on:click="supprFilm"> supprime le film </button>
      <button v-on:click="supprTxt">Supprime le txt </button> 
       <button v-on:click="changeTitre">Changer le titre</button> 

  </div>
     <slot name="info"></slot>
  </div>
</template>

<script>

import { bus } from "../../main";

export default {
    name: 'Liste' ,
    data: function () {
       
    },
    methods: {
        supprFilm : function(){
            this.myArr.pop()
        },
        supprTxt : function () {
            this.txt = ''
        },
        changeTitre : function () {
            bus.$emit('changeTitre', 'Le WolfKingSamy le baroudeur ' )
        }
    },
    props: ['myArr', 'txt'],

}
</script>

<style scoped src="./Liste.css">


</style>
