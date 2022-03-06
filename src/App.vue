<template>
  <formHandel />
  <methodHandeler />
  <conditionalRendering />  
  <bindData />
  <uttamKumar />
</template>

<script>
import uttamKumar from './components/Uttam.vue'
import bindData from './components/bind.vue'
import conditionalRendering from './components/conditionalRendering.vue'
import methodHandeler from './components/methodHandeler.vue'
import formHandel from './components/formhandel.vue'

export default {
  name: 'App',
  components: {
    uttamKumar,
    bindData,
    conditionalRendering,
    methodHandeler,
    formHandel,
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
  margin-top: 60px;
}
</style>
