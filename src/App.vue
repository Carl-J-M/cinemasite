<template>
  <div id="app">
    <landing-component/>
  </div>
</template>

<script>
import LandingComponent from './components/LandingComponent.vue'

export default {
  name: 'App',
  components: {
    "landing-component" : LandingComponent,
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}
</style>
