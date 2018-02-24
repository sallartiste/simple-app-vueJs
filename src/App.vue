<template>
  <div id="app">
      <citizens firstname="Erick" lastname="Salla" age="43 ans"></citizens>
  </div>
</template>

<script>
//import hello from './components/chap4.2/Hello.vue'
import citizens from './components/chap5/citizens.vue'

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
</style>
