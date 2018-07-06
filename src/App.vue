<template>
  <div id="app">
    <Heading/>
  </div>
</template>

<script>
import Heading from './components/Heading'

export default {
  name: 'App',
  components: {
    Heading
  }
}
</script>

<style>
#app {
  font-family: 'Signika', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ef5285;
  background-color:#a5dff9;
  height: 100vh;
}
</style>
