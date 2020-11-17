<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Header enterpriseName="Magic"/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header

  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  --full-white: #fff;
  --bg-white: #cccfd3;
  --orange: #F25C05;
  --dark-blue: #040D26;
  --hover-blue: #071540;
  --light-blue: #111C59; 
}

html {
  font-size: 62.5%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
