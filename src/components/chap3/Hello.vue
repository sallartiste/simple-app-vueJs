<template>
  <div>
    <img :src="img">
    <h1> Chap 3: Transmission d'une valeur d'un composant parent à un composant enfant</h1>
    <h2>Hello {{firstname}} {{lastname}} from {{from}} !!!</h2>
  </div>
</template>

<script>
export default {
   data (){
     return {
       //from: 'Rotterdam'
     }
   },
   props: ['firstname', 'lastname', 'from', 'img']
}
</script>

<style>
  h1{
    color:#c00;
  }
</style>
