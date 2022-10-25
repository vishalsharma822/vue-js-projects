<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <IfElse /> -->
  <TwoIfElse />
  <ToggleCondition />
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import IfElse from './components/IfElse.vue'
import TwoIfElse from './components/TwoIfElse.vue';
import ToggleCondition from './components/ToggleCondition.vue';

export default {
  name: 'App',
  components: {
    //HelloWorld,
    //IfElse,
    TwoIfElse,
    ToggleCondition
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
