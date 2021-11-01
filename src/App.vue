<template>
  <Duplicate/>
</template>

<script>
import Duplicate from "./components/Duplicate.vue"

export default {
  name: 'App',
  components: {
    Duplicate
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
*{
  box-sizing: border-box;
}

body{
  margin: 0;
}
html {
  scroll-behavior: smooth;
}
</style>
