<template>
  <div id="app">
    <navbar-comp />
  </div>
</template>

<script>
import navbarComp from "./components/navbar/navbarComp.vue";

export default {
  name: 'App',
  components: {
    navbarComp,
  }
}
</script>

<style>
  /* Import Open Sans Font */
  @import url('https://fonts.googleapis.com/css?family=Open+Sans&display=swap');
  
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
  }
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
