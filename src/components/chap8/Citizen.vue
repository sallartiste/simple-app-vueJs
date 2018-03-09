<template>
    <div id="citizen">
        <table>
                <tr><td>ID : {{citizen.id}}</td></tr>
                <tr><td>Firstname : {{citizen.firstname}}</td></tr>
                <tr><td>Lastname : {{citizen.lastname}}</td></tr>
                <tr><td>Birthdate : {{citizen.birthdate}}</td></tr>
                <tr><td>Age : {{citizen.age}}</td></tr>
                <tr><td>Email address : {{citizen.mail}}</td></tr>
                <tr><td>Phone nummer : {{citizen.phone}}</td></tr>
        </table>
    </div>
</template>

<script>
  import Vue from 'vue'
  import VueResource from 'vue-resource'
  Vue.use(VueResource)

  export default{
       data() {
           return {
               citizen: {}
           }
       },
       http : {
           root:'http://localhost:3000'
       },

       created(){
           bus.$on('selectedCitizen', (selectedCitizen) => {
               this.$resource('citizens{/id}/details').get({id:selectedCitizen}).then((response) => {
                   this.citizen = response.data[0]
               }, (response) => {
                   console.log('erreur', response)
               }
             )
           })
       }
  }

</script>

<style>
  h1{
    color:#c00;
  }
  table td{
      /*border: 1px solid grey;*/
  }

  #citizen{
      display: inline-block;
      width: 50%;
  }
</style>
