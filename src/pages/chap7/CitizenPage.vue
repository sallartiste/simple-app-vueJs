<template>
    <div id="page">
        <div id="head">
            <img src="../../assets/war.jpg">
            <h1> Chap 6: Transmission d'une valeur d'un composant enfant à un composant parent</h1>
        </div>
        <!--...-->
        <div id="content">
            <citizens></citizens>
            <citizen></citizen>
        </div>
    </div>
</template>

<script>
 import citizens from '../../components/chap7/Citizens.vue'
 import citizen from '../../components/chap7/Citizen.vue'

 export default {
    components: {citizens, citizen},
 }

</script>

<style>

</style>
