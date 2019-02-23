<template>
  <div id="app">
    <navigation/>
    <appheader />
    <appbody />
    <appfooter >Footer</appfooter>
  </div>
</template>

<script>
import navigation from './components/navigation/navigation.vue';
import appheader from './components/header/head.vue';
import appbody from './components/body/appbody.vue';
export default {
  name: 'app',
  components: {
    navigation,
    appheader,
    appbody
  }
}
</script>

<style>
*{
  margin: 0px;
  font-family: monospace;
}
body {
  height: 100vh;
}
#app {
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: auto minmax(310px, max-content) minmax(768px, max-content) 100px;
}
appfooter {
  background: orange;
}
</style>
