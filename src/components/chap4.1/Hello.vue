<template>
  <div>
    <img src="../../assets/war.jpg">
    <h1> Chap 4: Modifier des données d'un composant</h1>
    <h2>Hello {{person.firstname}} {{person.lastname}} from {{from}} !!!</h2>
    <label>Firstname: <input type="text" v-model="person.firstname"> </label><br />
    <label>Lastname: <input type="text" v-model="person.lastname"> </label><br>
    <label>From: <input type="text" v-model="from"> </label>
  </div>
</template>

<script>
export default {
   data (){
     return {
         person: {
             firstname: 'Lolo',
             lastname: 'Ferrari'
         },
         from: 'Kigali'
     }
   }

}
</script>

<style>
  h1{
    color:#c00;
  }
</style>
