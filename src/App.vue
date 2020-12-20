<template>
  <div id="app">
    <FormComponent/>
  </div>
</template>

<script>
import FormComponent from './components/FormComponent.vue'

export default {
  name: 'App',
  components: {
    FormComponent
  }
}
</script>

<style>
  body {
    margin: 0;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #C9D1D9;
    min-height: 100vh;
    background-color: #0D1117;
  }
</style>
