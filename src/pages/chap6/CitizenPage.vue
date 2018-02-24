<template>
    <div id="page">
        <div id="head">
            <img src="../../assets/war.jpg">
            <h1> Chap 6: Transmission d'une valeur d'un composant enfant à un composant parent</h1>
        </div>
        <!--...-->
        <div id="content">
            <citizens @selected="setSelected($event)"></citizens>
            <citizen :citizen="selectCitizen"></citizen>
        </div>
    </div>
</template>

<script>
 import citizens from '../../components/chap6/Citizens.vue'
 import citizen from '../../components/chap6/Citizen.vue'

 export default {
   data () {
       return {
           selectCitizen: {}
       }
   },

    components: {citizens, citizen},

    methods : {
        setSelected(selectCitizen){
            this.selectCitizen = selectCitizen
        }
    }
 }




</script>

<style>

</style>
