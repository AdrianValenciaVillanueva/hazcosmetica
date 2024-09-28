<template>
  <NavigationBar />
  <headC />
</template>

<script>
import NavigationBar from './components/NavigationBar.vue';
import headC from './components/headC.vue';


export default {
  name: 'App',
  components: {
    NavigationBar,
    headC,
  }
}
</script>

<style>

body{
  margin: 0;
  padding: 0;
  width: 100%;
  background-color: #f2f2f2;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  
}
</style>
