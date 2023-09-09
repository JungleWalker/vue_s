<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <InformationChoose/>
</template>

<script>

import InformationChoose from "@/components/InformationChoose.vue";

export default {
  name: 'App',
  components: {InformationChoose},
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
