<template>
  <div id="app">
      <citizens></citizens>
  </div>
</template>

<script>
//import hello from './components/chap4.2/Hello.vue'
import citizens from './pages/chap7/CitizenPage.vue'

export default {
  name: 'App',
  components: {
    citizens
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}
</style>
