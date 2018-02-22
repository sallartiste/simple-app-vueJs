<template>
  <div>
    <h1> Chap 2:Données d'un composant</h1>
    <h2>Hello {{person.firstname}} {{person.lastname}} from {{from}} !!!</h2>
  </div>
</template>

<script>
export default {
   data (){
     return {
       person:{
         firstname: 'Eric',
         lastname: 'Salla'
       },
       from: 'Rotterdam'
     }
   }
}
</script>

<style>
  h1{
    color:#c00;
  }
</style>
