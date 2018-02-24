<template>
    <div id="citizen">
        <table>
                <tr><td>ID : {{citizen.id}}</td></tr>
                <tr><td>Firstname : {{citizen.firstname}}</td></tr>
                <tr><td>Lastname : {{citizen.lastname}}</td></tr>
                <tr><td>Age : {{citizen.age}}</td></tr>
        </table>
    </div>
</template>

<script>

  export default{
       props: ['citizen']
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
