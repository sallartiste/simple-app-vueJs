<template>
    <div>
        <img src="../../assets/war.jpg">
        <h1> Chap 5: Invoquer un service avec REST</i></h1>
        <table>
            <tr v-for="citizen in citizens">
                <td>{{citizen.firstname}}</td>
                <td>{{citizen.lastname}}</td>
            </tr>
        </table>
        <button @click="addCitizens">Ajouter</button><br><br>
        <span>Le nombre de Habitans = {{counter}}</span>
    </div>
</template>

<script>
  import Vue from 'vue'
  import VueResource from 'vue-resource'
  Vue.use(VueResource)

  export default{
      data (){
          return{
              citizens: []
          }
      },
      http: {
          root: 'http://localhost:3000'
      },

      methods:{
          addCitizens(){
              this.citizens.push({"firstname":"T'Challa", "lastname":"Of Wakanda", "age":"30"})
          }
      },
      computed:{
          counter(){
              return this.citizens.length
          }
      },
      mounted(){
          this.$resource('citizens').get().then((response) => {
              this.citizens = response.data
          },(response) => {
              console.log('erreur', response);
          })
      }
  }

</script>

<style>
  h1{
    color:#c00;
  }
  table td{
      border: 1px solid grey;
  }
</style>
