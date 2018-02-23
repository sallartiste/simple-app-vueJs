<template>
    <div>
        <img src="../../assets/war.jpg">
        <h1> Chap 4.2: Model > vue: <i>Methods, computed, mounted, props</i></h1>
        <table>
            <tr v-for="citizen in citizens">
                <td>{{citizen.firstname}}</td>
                <td>{{citizen.lastname}}</td>
                <td>{{citizen.age}}</td>
            </tr>
        </table>
        <button @click="addCitizens">Ajouter</button><br><br>
        <span>Le nombre de Habitans = {{counter}}</span>
    </div>
</template>

<script>
  export default{
      data (){
          return{
              citizens: []
          }
      },
      props:["firstname", "lastname", "age"],
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
          this.citizens.push({
              "firstname":this.firstname, "lastname":this.lastname, "age":this.age
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
