<template>
  <div id="app">
    <hello firstname="Lloyd" lastname="Mangitukwa" from="Kinshasa" img="./static/shuri.jpg"></hello>
  </div>
</template>

<script>
import hello from './components/chap3/Hello.vue'

export default {
  name: 'App',
  components: {
    hello
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
